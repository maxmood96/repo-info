<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.36`](#telegraf136)
-	[`telegraf:1.36-alpine`](#telegraf136-alpine)
-	[`telegraf:1.36.4`](#telegraf1364)
-	[`telegraf:1.36.4-alpine`](#telegraf1364-alpine)
-	[`telegraf:1.37`](#telegraf137)
-	[`telegraf:1.37-alpine`](#telegraf137-alpine)
-	[`telegraf:1.37.3`](#telegraf1373)
-	[`telegraf:1.37.3-alpine`](#telegraf1373-alpine)
-	[`telegraf:1.38`](#telegraf138)
-	[`telegraf:1.38-alpine`](#telegraf138-alpine)
-	[`telegraf:1.38.1`](#telegraf1381)
-	[`telegraf:1.38.1-alpine`](#telegraf1381-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.36`

```console
$ docker pull telegraf@sha256:5d2317b59edc78cdeb7bd073eaccc3e6bfdc10118db06880f2dad550e91eff1d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36` - linux; amd64

```console
$ docker pull telegraf@sha256:47ad53ab085137864e262e1a39f07f1e10beacbc0c08b4cc1a05911c3bbb8dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (171950855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687604fe9c721cb036413014361078a576916c256ba43f534e60beac3857efec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:17:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:17:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Feb 2026 20:17:40 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 24 Feb 2026 20:17:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 24 Feb 2026 20:17:40 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 24 Feb 2026 20:17:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:17:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:17:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489e11c62566f0ad85344b7559bb78bcaf4b315d1b7bff843a03850fd884bbeb`  
		Last Modified: Tue, 24 Feb 2026 20:17:58 GMT  
		Size: 18.9 MB (18944364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5712141c0589a8a685e0a479a033cd0acdf800e7eaacb36d62985dc88720a08`  
		Last Modified: Tue, 24 Feb 2026 20:17:57 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1746ecc962d39333d323be7aa7124d10d3b09a2810caa5c6ff5df52ca68e86d5`  
		Last Modified: Tue, 24 Feb 2026 20:18:00 GMT  
		Size: 80.5 MB (80473584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f040ac70d6f94236f43533dc95477dd8cad744cdde579cf856d024a0c178e12d`  
		Last Modified: Tue, 24 Feb 2026 20:17:57 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:61099aacb32ebb28b0749a71aa3416975810f0be316eaf305dec05680b19e59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b047b9a37e6635dea3d355fbdb4e28e6798fc35bfcdb2189fa5b7f7e086562`

```dockerfile
```

-	Layers:
	-	`sha256:f843c6a9ac0c404aa02af50c305e5f664dd80e59eb4ae425eb64d35af322793f`  
		Last Modified: Tue, 24 Feb 2026 20:17:57 GMT  
		Size: 6.7 MB (6656103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3511caa44ab0f1d41ea1af381392ccc0bf0d7816c21ef9029e305aa465c8c579`  
		Last Modified: Tue, 24 Feb 2026 20:17:57 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:d53351578076a85069c6f70b1d09450a920541dd302ac55cb13839d705fc15a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157819098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95055526193ed34efff2642975166117041df048f70631c3a2decb95e46a1189`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:48:22 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:48:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Feb 2026 21:48:29 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 24 Feb 2026 21:48:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 24 Feb 2026 21:48:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 24 Feb 2026 21:48:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 21:48:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 21:48:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:510542cb38bcb0c99cf41f8715bc80ae2e63df19b8399efbb11254ee0ddd4299`  
		Last Modified: Tue, 24 Feb 2026 18:41:53 GMT  
		Size: 44.2 MB (44207818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122a79376a0d51f606a8d45c17043adef288961e7b30a2332c485fac0427d825`  
		Last Modified: Tue, 24 Feb 2026 20:01:59 GMT  
		Size: 21.9 MB (21942084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72205ce2f87d0f6da66bcae94dc93ab524d655bbf240dc432a432ea42fc2f1cc`  
		Last Modified: Tue, 24 Feb 2026 21:48:46 GMT  
		Size: 17.7 MB (17699877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cb9867a3640d4f5ae4f987d3ade09ad65fe232a1df038cf4d2432ba95b2b64`  
		Last Modified: Tue, 24 Feb 2026 21:48:45 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e0eb241462f167178b578352adb552e97d2c0a7a290ad96ca334de4bc1edfa`  
		Last Modified: Tue, 24 Feb 2026 21:48:47 GMT  
		Size: 74.0 MB (73963638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e20c1924dd93566043db76953cbc0acf006b01952b29fa498af335e328c17a`  
		Last Modified: Tue, 24 Feb 2026 21:48:45 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:3e4444d47b8323900df9695c1006f993c447447b1787975470562dabbef7be08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6665217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b70292270ffe2ecc6971dfc21a71643b5cb81de29e50facbe07f358221062d1`

```dockerfile
```

-	Layers:
	-	`sha256:fbc8da744cf4087a01e5d121bd745bea4a40787f4fb8b08c1fa1bda9297e6cd3`  
		Last Modified: Tue, 24 Feb 2026 21:48:45 GMT  
		Size: 6.7 MB (6650700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4377826fbfcbd0ea0bea6bdc1478bc05385ed11b7ea611135bce2aede8ce9888`  
		Last Modified: Tue, 24 Feb 2026 21:48:45 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:92370309f50c28fbe5b1884c22873078b7ab60d03d404bad00b3ca5741cf5a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162669765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90736bfab4a33cb2c9c4c97a06e4c0dc9d748fb8ffdb1e8214011166b2cb6a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:29:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:29:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Feb 2026 20:29:42 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 24 Feb 2026 20:29:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 24 Feb 2026 20:29:42 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 24 Feb 2026 20:29:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:29:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:29:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2b4e4b7ff25ca1933737ac0a836a484e7ba89c783c3480322d1546a2204329`  
		Last Modified: Tue, 24 Feb 2026 20:29:59 GMT  
		Size: 18.9 MB (18885793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15763733d84aeaeb82a21f39b4fde55b8edb3ce940427f153b100e38b528868b`  
		Last Modified: Tue, 24 Feb 2026 20:29:58 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d2812c09159db5bff1365f1bc09a8bb07f65fb7cf1c9235e0a8c6e3e33e0db`  
		Last Modified: Tue, 24 Feb 2026 20:30:01 GMT  
		Size: 71.8 MB (71800350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c283eb97282d7c6ba682a588b422f75fc91bc227ed7e52e54c883f7e44a275b4`  
		Last Modified: Tue, 24 Feb 2026 20:29:58 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:26fb01fddc58844abdd9453464231d51fbe32ca8eefcf121e6f226c47a4283fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac3780d6fbe57a457797bbfeb11bbe25d3bd9c849bd48f496c97fe7b1aad2a6`

```dockerfile
```

-	Layers:
	-	`sha256:2b74d0a5ed60259a9801c2c71e60e98111242ed89aed9baa2586ee9aafb5bce2`  
		Last Modified: Tue, 24 Feb 2026 20:29:59 GMT  
		Size: 6.7 MB (6656779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:378a7797e413ba5395900ba575995a2881127d1fc1d95c61a044f5e875941b60`  
		Last Modified: Tue, 24 Feb 2026 20:29:58 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36-alpine`

```console
$ docker pull telegraf@sha256:74614dd18bd8c984d8d5423d6c362da8b9a0c32543f9932660f03c1e8ae22893
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7e104d74dd7644a3f52e10b68cf4972907df0e16d541772b9da2cd987768f243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86645547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541b370deeda7910ea7253b472ecc2c000614befbc68504928d0ace6afb8ac2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:49:47 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b7d7273f9660e4714a4f3a80280881a133da7a4b266dd62099a308eb162f72`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28aadc15040b0a36abb07e3769a9f303cb26e56ef3f0d93b8d67305467d8fd`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 2.6 MB (2563616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc81e34cf097b50b7dd067c2614b05e26095fb2414a929a91855343b1d90a521`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 80.3 MB (80276156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661496d98862b6bcadcc878a91c0481a10a977bd7484506964f0fa597e847e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a58b7e8c82dd5051261d6c864d491aeea150486c9e1f27c7ee855fb6a31203aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48411f51293ab3606c49c94104046ecf052e493bbfcfe2f480129ab5409030c`

```dockerfile
```

-	Layers:
	-	`sha256:da625155b1394d0acc62042503f8abc1c81a442603c6d3593589a8d4a55f6341`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 1.1 MB (1142308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de3d21cf0caad0d90bd450ac8df7e7d30e8f0aad489474e9e436f77f5ade2fca`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:83bc8287ed0eb1b80b20475a90d070e187731561e718f2dd3895fe06431022eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78367221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eb1f6fb6136da60a3f40864a08a135e84bee5208c5d660116eebe674366a33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:56:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:56:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:56:13 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091ad53e26795247908fee75f1fec45378bfe7b9ed2893274f93b24025ac8c82`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9006dcde8e9ae246bba52f47cf327cff96c0b85caea2b7bb7c9054ff07b9d3`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 2.6 MB (2627637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9571296956dfa14bf2102b6281cfc90613780a517750c02daae06df9c48984`  
		Last Modified: Wed, 28 Jan 2026 03:56:29 GMT  
		Size: 71.6 MB (71599165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c402cd3a778e5774ca08af5f6640eaf81bb54e3bf015248f992dc3bedf0c94b6`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8ae6952c3c19ba215996ca8b6bd4634c696319744b633dceb09a71bf50bdd603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1152962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71490915f7d134e9704e5bc89bfda33a5b8c3561ce98c890715d964fc114d237`

```dockerfile
```

-	Layers:
	-	`sha256:df6dda659050fe9d9dda0bd1f9f03b6be5573bf09cac3651532af6a2c3d3d82a`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 1.1 MB (1137935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c95dceab1d5fe3c1330859a4271ff252f83fe230c9b155b95b00d6ee2a76c2`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 15.0 KB (15027 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4`

```console
$ docker pull telegraf@sha256:5d2317b59edc78cdeb7bd073eaccc3e6bfdc10118db06880f2dad550e91eff1d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.4` - linux; amd64

```console
$ docker pull telegraf@sha256:47ad53ab085137864e262e1a39f07f1e10beacbc0c08b4cc1a05911c3bbb8dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (171950855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687604fe9c721cb036413014361078a576916c256ba43f534e60beac3857efec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:17:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:17:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Feb 2026 20:17:40 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 24 Feb 2026 20:17:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 24 Feb 2026 20:17:40 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 24 Feb 2026 20:17:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:17:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:17:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489e11c62566f0ad85344b7559bb78bcaf4b315d1b7bff843a03850fd884bbeb`  
		Last Modified: Tue, 24 Feb 2026 20:17:58 GMT  
		Size: 18.9 MB (18944364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5712141c0589a8a685e0a479a033cd0acdf800e7eaacb36d62985dc88720a08`  
		Last Modified: Tue, 24 Feb 2026 20:17:57 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1746ecc962d39333d323be7aa7124d10d3b09a2810caa5c6ff5df52ca68e86d5`  
		Last Modified: Tue, 24 Feb 2026 20:18:00 GMT  
		Size: 80.5 MB (80473584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f040ac70d6f94236f43533dc95477dd8cad744cdde579cf856d024a0c178e12d`  
		Last Modified: Tue, 24 Feb 2026 20:17:57 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:61099aacb32ebb28b0749a71aa3416975810f0be316eaf305dec05680b19e59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b047b9a37e6635dea3d355fbdb4e28e6798fc35bfcdb2189fa5b7f7e086562`

```dockerfile
```

-	Layers:
	-	`sha256:f843c6a9ac0c404aa02af50c305e5f664dd80e59eb4ae425eb64d35af322793f`  
		Last Modified: Tue, 24 Feb 2026 20:17:57 GMT  
		Size: 6.7 MB (6656103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3511caa44ab0f1d41ea1af381392ccc0bf0d7816c21ef9029e305aa465c8c579`  
		Last Modified: Tue, 24 Feb 2026 20:17:57 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:d53351578076a85069c6f70b1d09450a920541dd302ac55cb13839d705fc15a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157819098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95055526193ed34efff2642975166117041df048f70631c3a2decb95e46a1189`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:48:22 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:48:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Feb 2026 21:48:29 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 24 Feb 2026 21:48:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 24 Feb 2026 21:48:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 24 Feb 2026 21:48:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 21:48:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 21:48:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:510542cb38bcb0c99cf41f8715bc80ae2e63df19b8399efbb11254ee0ddd4299`  
		Last Modified: Tue, 24 Feb 2026 18:41:53 GMT  
		Size: 44.2 MB (44207818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122a79376a0d51f606a8d45c17043adef288961e7b30a2332c485fac0427d825`  
		Last Modified: Tue, 24 Feb 2026 20:01:59 GMT  
		Size: 21.9 MB (21942084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72205ce2f87d0f6da66bcae94dc93ab524d655bbf240dc432a432ea42fc2f1cc`  
		Last Modified: Tue, 24 Feb 2026 21:48:46 GMT  
		Size: 17.7 MB (17699877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cb9867a3640d4f5ae4f987d3ade09ad65fe232a1df038cf4d2432ba95b2b64`  
		Last Modified: Tue, 24 Feb 2026 21:48:45 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e0eb241462f167178b578352adb552e97d2c0a7a290ad96ca334de4bc1edfa`  
		Last Modified: Tue, 24 Feb 2026 21:48:47 GMT  
		Size: 74.0 MB (73963638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e20c1924dd93566043db76953cbc0acf006b01952b29fa498af335e328c17a`  
		Last Modified: Tue, 24 Feb 2026 21:48:45 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:3e4444d47b8323900df9695c1006f993c447447b1787975470562dabbef7be08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6665217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b70292270ffe2ecc6971dfc21a71643b5cb81de29e50facbe07f358221062d1`

```dockerfile
```

-	Layers:
	-	`sha256:fbc8da744cf4087a01e5d121bd745bea4a40787f4fb8b08c1fa1bda9297e6cd3`  
		Last Modified: Tue, 24 Feb 2026 21:48:45 GMT  
		Size: 6.7 MB (6650700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4377826fbfcbd0ea0bea6bdc1478bc05385ed11b7ea611135bce2aede8ce9888`  
		Last Modified: Tue, 24 Feb 2026 21:48:45 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:92370309f50c28fbe5b1884c22873078b7ab60d03d404bad00b3ca5741cf5a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162669765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90736bfab4a33cb2c9c4c97a06e4c0dc9d748fb8ffdb1e8214011166b2cb6a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:29:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:29:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Feb 2026 20:29:42 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 24 Feb 2026 20:29:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 24 Feb 2026 20:29:42 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 24 Feb 2026 20:29:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:29:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:29:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2b4e4b7ff25ca1933737ac0a836a484e7ba89c783c3480322d1546a2204329`  
		Last Modified: Tue, 24 Feb 2026 20:29:59 GMT  
		Size: 18.9 MB (18885793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15763733d84aeaeb82a21f39b4fde55b8edb3ce940427f153b100e38b528868b`  
		Last Modified: Tue, 24 Feb 2026 20:29:58 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d2812c09159db5bff1365f1bc09a8bb07f65fb7cf1c9235e0a8c6e3e33e0db`  
		Last Modified: Tue, 24 Feb 2026 20:30:01 GMT  
		Size: 71.8 MB (71800350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c283eb97282d7c6ba682a588b422f75fc91bc227ed7e52e54c883f7e44a275b4`  
		Last Modified: Tue, 24 Feb 2026 20:29:58 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:26fb01fddc58844abdd9453464231d51fbe32ca8eefcf121e6f226c47a4283fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac3780d6fbe57a457797bbfeb11bbe25d3bd9c849bd48f496c97fe7b1aad2a6`

```dockerfile
```

-	Layers:
	-	`sha256:2b74d0a5ed60259a9801c2c71e60e98111242ed89aed9baa2586ee9aafb5bce2`  
		Last Modified: Tue, 24 Feb 2026 20:29:59 GMT  
		Size: 6.7 MB (6656779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:378a7797e413ba5395900ba575995a2881127d1fc1d95c61a044f5e875941b60`  
		Last Modified: Tue, 24 Feb 2026 20:29:58 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4-alpine`

```console
$ docker pull telegraf@sha256:74614dd18bd8c984d8d5423d6c362da8b9a0c32543f9932660f03c1e8ae22893
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7e104d74dd7644a3f52e10b68cf4972907df0e16d541772b9da2cd987768f243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86645547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541b370deeda7910ea7253b472ecc2c000614befbc68504928d0ace6afb8ac2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:49:47 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b7d7273f9660e4714a4f3a80280881a133da7a4b266dd62099a308eb162f72`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28aadc15040b0a36abb07e3769a9f303cb26e56ef3f0d93b8d67305467d8fd`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 2.6 MB (2563616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc81e34cf097b50b7dd067c2614b05e26095fb2414a929a91855343b1d90a521`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 80.3 MB (80276156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661496d98862b6bcadcc878a91c0481a10a977bd7484506964f0fa597e847e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a58b7e8c82dd5051261d6c864d491aeea150486c9e1f27c7ee855fb6a31203aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48411f51293ab3606c49c94104046ecf052e493bbfcfe2f480129ab5409030c`

```dockerfile
```

-	Layers:
	-	`sha256:da625155b1394d0acc62042503f8abc1c81a442603c6d3593589a8d4a55f6341`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 1.1 MB (1142308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de3d21cf0caad0d90bd450ac8df7e7d30e8f0aad489474e9e436f77f5ade2fca`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:83bc8287ed0eb1b80b20475a90d070e187731561e718f2dd3895fe06431022eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78367221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eb1f6fb6136da60a3f40864a08a135e84bee5208c5d660116eebe674366a33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:56:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:56:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:56:13 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091ad53e26795247908fee75f1fec45378bfe7b9ed2893274f93b24025ac8c82`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9006dcde8e9ae246bba52f47cf327cff96c0b85caea2b7bb7c9054ff07b9d3`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 2.6 MB (2627637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9571296956dfa14bf2102b6281cfc90613780a517750c02daae06df9c48984`  
		Last Modified: Wed, 28 Jan 2026 03:56:29 GMT  
		Size: 71.6 MB (71599165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c402cd3a778e5774ca08af5f6640eaf81bb54e3bf015248f992dc3bedf0c94b6`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8ae6952c3c19ba215996ca8b6bd4634c696319744b633dceb09a71bf50bdd603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1152962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71490915f7d134e9704e5bc89bfda33a5b8c3561ce98c890715d964fc114d237`

```dockerfile
```

-	Layers:
	-	`sha256:df6dda659050fe9d9dda0bd1f9f03b6be5573bf09cac3651532af6a2c3d3d82a`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 1.1 MB (1137935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c95dceab1d5fe3c1330859a4271ff252f83fe230c9b155b95b00d6ee2a76c2`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 15.0 KB (15027 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37`

```console
$ docker pull telegraf@sha256:6aa6970c52c86d0dac03a66dc6d8daac7a7852b31648e5e4575859bc271df924
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37` - linux; amd64

```console
$ docker pull telegraf@sha256:5a7d27714e297375d7d414e2a54198ea60d0ca5e1bb8f77c7d3cd6b3909c4cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172260657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd3ed174f67285ecaefe70614a104e022f7f98233dfde5a3cf00b482fa785e5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:17:45 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:17:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Feb 2026 20:17:49 GMT
ENV TELEGRAF_VERSION=1.37.3
# Tue, 24 Feb 2026 20:17:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 24 Feb 2026 20:17:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 24 Feb 2026 20:17:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:17:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:17:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef759a9161a5bc2aaf99b1c374e1f29cd491638e86d87f4de73e1dd608160d8`  
		Last Modified: Tue, 24 Feb 2026 20:18:09 GMT  
		Size: 18.9 MB (18944511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45e97defe9672f0d0cb2a25296186000c37d3382ab936489665c3791c2809e9`  
		Last Modified: Tue, 24 Feb 2026 20:18:08 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37142fd6b39def08713aaadbd85ee0135cd8ba09d9dc0fc4fd5453f0c4cceb3`  
		Last Modified: Tue, 24 Feb 2026 20:18:11 GMT  
		Size: 80.8 MB (80783226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01ec17b69ac59e1614051b6340a1887a3fb8171cc83e869473a58b7d4a6a4e5`  
		Last Modified: Tue, 24 Feb 2026 20:18:08 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:68dc919e87429f0a5cc089de451b8f0e94d1bb6c610cdefccb2d1dd1fe10ebac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab6090badf740bdad79f38d940483b2f3d3011ba91a4122ef1925e12c1abe8d`

```dockerfile
```

-	Layers:
	-	`sha256:1c0d272850dca2d5ece36593d6cc70802abc360b184757c45e912bbba9c518a8`  
		Last Modified: Tue, 24 Feb 2026 20:18:08 GMT  
		Size: 6.7 MB (6667260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6481b6246ca9656009a688bb6daa3effe0f3f7679d725c74f8d17b0bfaf05576`  
		Last Modified: Tue, 24 Feb 2026 20:18:08 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:fea3e568b468a35f38e55fb606dd7391ae8e93c1e08c0dee6668827caed58a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158472791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abddac12261d30e483e5300973c92c40a6490acf1ae6d77fc5ca920ad044421`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:48:25 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:48:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Feb 2026 21:48:30 GMT
ENV TELEGRAF_VERSION=1.37.3
# Tue, 24 Feb 2026 21:48:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 24 Feb 2026 21:48:30 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 24 Feb 2026 21:48:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 21:48:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 21:48:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:510542cb38bcb0c99cf41f8715bc80ae2e63df19b8399efbb11254ee0ddd4299`  
		Last Modified: Tue, 24 Feb 2026 18:41:53 GMT  
		Size: 44.2 MB (44207818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122a79376a0d51f606a8d45c17043adef288961e7b30a2332c485fac0427d825`  
		Last Modified: Tue, 24 Feb 2026 20:01:59 GMT  
		Size: 21.9 MB (21942084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107a04fa5a210877ce9d9a4c666034749b7bac2c6563260ec9aa61b2d420a4ea`  
		Last Modified: Tue, 24 Feb 2026 21:48:50 GMT  
		Size: 17.7 MB (17699791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf94ed756373cad9c2a4050e1d679e9264bc7afe609c032dfce5539280855460`  
		Last Modified: Tue, 24 Feb 2026 21:48:50 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d34ec95b941e7bc1a188528c915e9318d020d42813487977adcdd94168127ae`  
		Last Modified: Tue, 24 Feb 2026 21:48:52 GMT  
		Size: 74.6 MB (74617419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4139690a3ce82fe9fe55d9ac4e47d02abbe055c474e3dd49c68c1145edbf7e9`  
		Last Modified: Tue, 24 Feb 2026 21:48:50 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:734f254167868747d224ddba318a8e859356cf819a2f386e0f0c011e30d7ee06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb159b9df8096c2855986cfd3ad21d366616002617484ad95abda3442c55230`

```dockerfile
```

-	Layers:
	-	`sha256:6833a080a67634bb4daa7868d20aba2a96fdc80021eaa109c6a88c38d0b7c2a1`  
		Last Modified: Tue, 24 Feb 2026 21:48:50 GMT  
		Size: 6.7 MB (6661865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40944a31097d427e0a55eee2c65b54dac78eb4ce98da1d29446a436ab6afada`  
		Last Modified: Tue, 24 Feb 2026 21:48:49 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c29a49f4dfe7cffa080d47c8d9ec4e69130ece52a5981d0501856e45fa20928e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163040532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67519b2269e2e7dd7b21494cf55f77152284d3801557d39d93e0b40a70a6dc00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:29:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:29:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Feb 2026 20:29:48 GMT
ENV TELEGRAF_VERSION=1.37.3
# Tue, 24 Feb 2026 20:29:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 24 Feb 2026 20:29:48 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 24 Feb 2026 20:29:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:29:48 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f39554b7ff8e05e4542a89f81c97a7115e5c4c03f7c14cc1a7b52833c5e7b29`  
		Last Modified: Tue, 24 Feb 2026 20:30:08 GMT  
		Size: 18.9 MB (18885876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d1e2a08bcaac9e0ceffacb0564490faedada2d627606ec3fa61477aab013b3`  
		Last Modified: Tue, 24 Feb 2026 20:30:07 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100dae0ed224a89c8dfb0fd71f59550d2c9039b5c6582c7694cb4bd665e5daa1`  
		Last Modified: Tue, 24 Feb 2026 20:30:09 GMT  
		Size: 72.2 MB (72171019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedfa99099052bcc2a3b244d3c1d0dd92b9190f0def6b9df24bfe240e0dca999`  
		Last Modified: Tue, 24 Feb 2026 20:30:07 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:d445c9ee1d1cf7237ac19534ae162328816224a3644798b9bbbd0f645a3c7208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4f721db13793cdb591cad553a4ad91595e9423109b0b0a23a0213e5ca50451`

```dockerfile
```

-	Layers:
	-	`sha256:ec6bb6887ff037927b956337a648ba9d53c2c4d4e75d75c0756ca384e6379421`  
		Last Modified: Tue, 24 Feb 2026 20:30:07 GMT  
		Size: 6.7 MB (6667948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:903d849b177712fd50cdfbfbb68f4cc32ae8d663fe5ee6bcdf35ae1b8d79f8b1`  
		Last Modified: Tue, 24 Feb 2026 20:30:06 GMT  
		Size: 14.8 KB (14850 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37-alpine`

```console
$ docker pull telegraf@sha256:a550e63a2efbea4b49596e475f0fcd3b057ff2ab0dfc8102357de289ee342a37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:fba66fd8b08dc6e56336289fd91c0b9c055b5431b1ac6f0cb3c5b0203b24d450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86946044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38efb96d204dcce61a2419f13705ddf967966bbf6c20b8dc214d6cd4917df5cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 22:13:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 23 Feb 2026 22:13:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 23 Feb 2026 22:13:15 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 23 Feb 2026 22:13:15 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 23 Feb 2026 22:13:15 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Feb 2026 22:13:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Feb 2026 22:13:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 22:13:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b56c151750e24306076f9157dce93616ec037d271702f125dc64fbf3376f8`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff331311971b9e1b3df00d187242872c6a7167b0fa5eb1b83bf07f57f6bd227`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 2.6 MB (2563613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b176fa3df8ddfa0c79b45cb78b9caf938ca77b7d56b923cdb8d9280c85548`  
		Last Modified: Mon, 23 Feb 2026 22:13:33 GMT  
		Size: 80.6 MB (80576658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a622797146e400edbb8a20860c8044210bb4ddf360b881dd59f657a0178e56`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:dbaf7ed8916c29f7e0e480a7ad699dbc11e6ff21f59b298ac7bc4c687f919ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b161c64ca482da5f21d71566f132f54ee64beb84f28a79454afce77c61e7ad74`

```dockerfile
```

-	Layers:
	-	`sha256:0ad1ed01319ca47cfb93e453ec6fce2996425a3ef91fb812891757a8a27d72c6`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 1.2 MB (1153465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:841e3534e20e0f7236187feb211ea64b35f00fbef79dd247d04d44865d348a5d`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 15.2 KB (15218 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f27c6f05cce7d68495838dcbbe51d1995f3ba235846d6753718f5b2cd8a7f603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78730556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5048f1f9cdf423929349c19bb659110cd4c7e1ab38dff7597763063c5a1978b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 22:12:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 23 Feb 2026 22:12:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 23 Feb 2026 22:12:09 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 23 Feb 2026 22:12:09 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 23 Feb 2026 22:12:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Feb 2026 22:12:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Feb 2026 22:12:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 22:12:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f365fa2017a849f86d84f3f3776e527b8ff2fb4628dfa52b2e2726747ba9a5f`  
		Last Modified: Mon, 23 Feb 2026 22:12:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dde69daba6471771a33e89fc18e2ef827eac0bbebbfa518372b5614a4c5072`  
		Last Modified: Mon, 23 Feb 2026 22:12:23 GMT  
		Size: 2.6 MB (2627610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fb53f42b0075065a38f3acdda1775b06ee78f844307d7125a10b6688253f62`  
		Last Modified: Mon, 23 Feb 2026 22:12:24 GMT  
		Size: 72.0 MB (71962529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d896748b58358906c78fda48ddade4bd1df0e660097580f49b6f08d0bb041131`  
		Last Modified: Mon, 23 Feb 2026 22:12:22 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f2ad750ecb35ac8a316aa4496da66885dfc42a651a503859707823f2d6f4ca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b3b3372362c4275569df86547f57711280021d198691725283f623157d5487`

```dockerfile
```

-	Layers:
	-	`sha256:84a7770deb78578c6e010d0e4268d870b145b32e787666e68441fd2377878852`  
		Last Modified: Mon, 23 Feb 2026 22:12:22 GMT  
		Size: 1.1 MB (1149104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b83295c00d09abd5a3a9c39ebd649a814a4169ff62cc5041580c6c7c1bfd6e5`  
		Last Modified: Mon, 23 Feb 2026 22:12:23 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.3`

```console
$ docker pull telegraf@sha256:6aa6970c52c86d0dac03a66dc6d8daac7a7852b31648e5e4575859bc271df924
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.3` - linux; amd64

```console
$ docker pull telegraf@sha256:5a7d27714e297375d7d414e2a54198ea60d0ca5e1bb8f77c7d3cd6b3909c4cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172260657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd3ed174f67285ecaefe70614a104e022f7f98233dfde5a3cf00b482fa785e5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:17:45 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:17:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Feb 2026 20:17:49 GMT
ENV TELEGRAF_VERSION=1.37.3
# Tue, 24 Feb 2026 20:17:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 24 Feb 2026 20:17:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 24 Feb 2026 20:17:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:17:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:17:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef759a9161a5bc2aaf99b1c374e1f29cd491638e86d87f4de73e1dd608160d8`  
		Last Modified: Tue, 24 Feb 2026 20:18:09 GMT  
		Size: 18.9 MB (18944511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45e97defe9672f0d0cb2a25296186000c37d3382ab936489665c3791c2809e9`  
		Last Modified: Tue, 24 Feb 2026 20:18:08 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37142fd6b39def08713aaadbd85ee0135cd8ba09d9dc0fc4fd5453f0c4cceb3`  
		Last Modified: Tue, 24 Feb 2026 20:18:11 GMT  
		Size: 80.8 MB (80783226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01ec17b69ac59e1614051b6340a1887a3fb8171cc83e869473a58b7d4a6a4e5`  
		Last Modified: Tue, 24 Feb 2026 20:18:08 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:68dc919e87429f0a5cc089de451b8f0e94d1bb6c610cdefccb2d1dd1fe10ebac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab6090badf740bdad79f38d940483b2f3d3011ba91a4122ef1925e12c1abe8d`

```dockerfile
```

-	Layers:
	-	`sha256:1c0d272850dca2d5ece36593d6cc70802abc360b184757c45e912bbba9c518a8`  
		Last Modified: Tue, 24 Feb 2026 20:18:08 GMT  
		Size: 6.7 MB (6667260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6481b6246ca9656009a688bb6daa3effe0f3f7679d725c74f8d17b0bfaf05576`  
		Last Modified: Tue, 24 Feb 2026 20:18:08 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:fea3e568b468a35f38e55fb606dd7391ae8e93c1e08c0dee6668827caed58a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158472791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abddac12261d30e483e5300973c92c40a6490acf1ae6d77fc5ca920ad044421`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:48:25 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:48:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Feb 2026 21:48:30 GMT
ENV TELEGRAF_VERSION=1.37.3
# Tue, 24 Feb 2026 21:48:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 24 Feb 2026 21:48:30 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 24 Feb 2026 21:48:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 21:48:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 21:48:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:510542cb38bcb0c99cf41f8715bc80ae2e63df19b8399efbb11254ee0ddd4299`  
		Last Modified: Tue, 24 Feb 2026 18:41:53 GMT  
		Size: 44.2 MB (44207818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122a79376a0d51f606a8d45c17043adef288961e7b30a2332c485fac0427d825`  
		Last Modified: Tue, 24 Feb 2026 20:01:59 GMT  
		Size: 21.9 MB (21942084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107a04fa5a210877ce9d9a4c666034749b7bac2c6563260ec9aa61b2d420a4ea`  
		Last Modified: Tue, 24 Feb 2026 21:48:50 GMT  
		Size: 17.7 MB (17699791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf94ed756373cad9c2a4050e1d679e9264bc7afe609c032dfce5539280855460`  
		Last Modified: Tue, 24 Feb 2026 21:48:50 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d34ec95b941e7bc1a188528c915e9318d020d42813487977adcdd94168127ae`  
		Last Modified: Tue, 24 Feb 2026 21:48:52 GMT  
		Size: 74.6 MB (74617419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4139690a3ce82fe9fe55d9ac4e47d02abbe055c474e3dd49c68c1145edbf7e9`  
		Last Modified: Tue, 24 Feb 2026 21:48:50 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:734f254167868747d224ddba318a8e859356cf819a2f386e0f0c011e30d7ee06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb159b9df8096c2855986cfd3ad21d366616002617484ad95abda3442c55230`

```dockerfile
```

-	Layers:
	-	`sha256:6833a080a67634bb4daa7868d20aba2a96fdc80021eaa109c6a88c38d0b7c2a1`  
		Last Modified: Tue, 24 Feb 2026 21:48:50 GMT  
		Size: 6.7 MB (6661865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40944a31097d427e0a55eee2c65b54dac78eb4ce98da1d29446a436ab6afada`  
		Last Modified: Tue, 24 Feb 2026 21:48:49 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c29a49f4dfe7cffa080d47c8d9ec4e69130ece52a5981d0501856e45fa20928e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163040532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67519b2269e2e7dd7b21494cf55f77152284d3801557d39d93e0b40a70a6dc00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:29:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:29:45 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Feb 2026 20:29:48 GMT
ENV TELEGRAF_VERSION=1.37.3
# Tue, 24 Feb 2026 20:29:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 24 Feb 2026 20:29:48 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 24 Feb 2026 20:29:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:29:48 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f39554b7ff8e05e4542a89f81c97a7115e5c4c03f7c14cc1a7b52833c5e7b29`  
		Last Modified: Tue, 24 Feb 2026 20:30:08 GMT  
		Size: 18.9 MB (18885876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d1e2a08bcaac9e0ceffacb0564490faedada2d627606ec3fa61477aab013b3`  
		Last Modified: Tue, 24 Feb 2026 20:30:07 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100dae0ed224a89c8dfb0fd71f59550d2c9039b5c6582c7694cb4bd665e5daa1`  
		Last Modified: Tue, 24 Feb 2026 20:30:09 GMT  
		Size: 72.2 MB (72171019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedfa99099052bcc2a3b244d3c1d0dd92b9190f0def6b9df24bfe240e0dca999`  
		Last Modified: Tue, 24 Feb 2026 20:30:07 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:d445c9ee1d1cf7237ac19534ae162328816224a3644798b9bbbd0f645a3c7208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4f721db13793cdb591cad553a4ad91595e9423109b0b0a23a0213e5ca50451`

```dockerfile
```

-	Layers:
	-	`sha256:ec6bb6887ff037927b956337a648ba9d53c2c4d4e75d75c0756ca384e6379421`  
		Last Modified: Tue, 24 Feb 2026 20:30:07 GMT  
		Size: 6.7 MB (6667948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:903d849b177712fd50cdfbfbb68f4cc32ae8d663fe5ee6bcdf35ae1b8d79f8b1`  
		Last Modified: Tue, 24 Feb 2026 20:30:06 GMT  
		Size: 14.8 KB (14850 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.3-alpine`

```console
$ docker pull telegraf@sha256:a550e63a2efbea4b49596e475f0fcd3b057ff2ab0dfc8102357de289ee342a37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:fba66fd8b08dc6e56336289fd91c0b9c055b5431b1ac6f0cb3c5b0203b24d450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86946044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38efb96d204dcce61a2419f13705ddf967966bbf6c20b8dc214d6cd4917df5cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 22:13:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 23 Feb 2026 22:13:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 23 Feb 2026 22:13:15 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 23 Feb 2026 22:13:15 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 23 Feb 2026 22:13:15 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Feb 2026 22:13:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Feb 2026 22:13:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 22:13:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b56c151750e24306076f9157dce93616ec037d271702f125dc64fbf3376f8`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff331311971b9e1b3df00d187242872c6a7167b0fa5eb1b83bf07f57f6bd227`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 2.6 MB (2563613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b176fa3df8ddfa0c79b45cb78b9caf938ca77b7d56b923cdb8d9280c85548`  
		Last Modified: Mon, 23 Feb 2026 22:13:33 GMT  
		Size: 80.6 MB (80576658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a622797146e400edbb8a20860c8044210bb4ddf360b881dd59f657a0178e56`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:dbaf7ed8916c29f7e0e480a7ad699dbc11e6ff21f59b298ac7bc4c687f919ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b161c64ca482da5f21d71566f132f54ee64beb84f28a79454afce77c61e7ad74`

```dockerfile
```

-	Layers:
	-	`sha256:0ad1ed01319ca47cfb93e453ec6fce2996425a3ef91fb812891757a8a27d72c6`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 1.2 MB (1153465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:841e3534e20e0f7236187feb211ea64b35f00fbef79dd247d04d44865d348a5d`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 15.2 KB (15218 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f27c6f05cce7d68495838dcbbe51d1995f3ba235846d6753718f5b2cd8a7f603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78730556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5048f1f9cdf423929349c19bb659110cd4c7e1ab38dff7597763063c5a1978b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 22:12:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 23 Feb 2026 22:12:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 23 Feb 2026 22:12:09 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 23 Feb 2026 22:12:09 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 23 Feb 2026 22:12:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Feb 2026 22:12:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Feb 2026 22:12:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 22:12:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f365fa2017a849f86d84f3f3776e527b8ff2fb4628dfa52b2e2726747ba9a5f`  
		Last Modified: Mon, 23 Feb 2026 22:12:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dde69daba6471771a33e89fc18e2ef827eac0bbebbfa518372b5614a4c5072`  
		Last Modified: Mon, 23 Feb 2026 22:12:23 GMT  
		Size: 2.6 MB (2627610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fb53f42b0075065a38f3acdda1775b06ee78f844307d7125a10b6688253f62`  
		Last Modified: Mon, 23 Feb 2026 22:12:24 GMT  
		Size: 72.0 MB (71962529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d896748b58358906c78fda48ddade4bd1df0e660097580f49b6f08d0bb041131`  
		Last Modified: Mon, 23 Feb 2026 22:12:22 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f2ad750ecb35ac8a316aa4496da66885dfc42a651a503859707823f2d6f4ca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b3b3372362c4275569df86547f57711280021d198691725283f623157d5487`

```dockerfile
```

-	Layers:
	-	`sha256:84a7770deb78578c6e010d0e4268d870b145b32e787666e68441fd2377878852`  
		Last Modified: Mon, 23 Feb 2026 22:12:22 GMT  
		Size: 1.1 MB (1149104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b83295c00d09abd5a3a9c39ebd649a814a4169ff62cc5041580c6c7c1bfd6e5`  
		Last Modified: Mon, 23 Feb 2026 22:12:23 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38`

```console
$ docker pull telegraf@sha256:b7c11b83c594a660d89ff86e745405035734fc33857bbadde550d07f8452629b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38` - linux; amd64

```console
$ docker pull telegraf@sha256:24a87b4118d623e434000bbf0e8c77b3e4d1bcb9d45747728c94d40f6d2e0016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172649887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c517bb8ced7edf8a7cc3b1e703dc9ac1c18b92675999bfb37ded301ac90f862`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 21:49:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 21:49:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Mar 2026 21:49:28 GMT
ENV TELEGRAF_VERSION=1.38.0
# Mon, 09 Mar 2026 21:49:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Mar 2026 21:49:28 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Mar 2026 21:49:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Mar 2026 21:49:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Mar 2026 21:49:28 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c50ce151bfa926c59b4224aadf63a506b9f97bd82366e3527cc332b7b291b30`  
		Last Modified: Mon, 09 Mar 2026 21:49:46 GMT  
		Size: 18.9 MB (18944455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434659474c2b3d691943ef0eb09fda91f8b28d10db480ebe4d907e3b68b68365`  
		Last Modified: Mon, 09 Mar 2026 21:49:45 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1965c1cf786e3766ad23e21994fec7ceaff39e245491620b59eb686fb9d51a79`  
		Last Modified: Mon, 09 Mar 2026 21:49:48 GMT  
		Size: 81.2 MB (81172510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1e3c216f806b640485ca8ff1cba0d4d0150ae736435b92f82ceb6c5bf7f77e`  
		Last Modified: Mon, 09 Mar 2026 21:49:45 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:5816d7a55657ecd2dd95064da98a5381ef1b27a510e91eb41fbe06e5f5f7ff4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af52e79e49a3062640b3a36deba37a4d006311f3c340d0d791ae406562f39d6b`

```dockerfile
```

-	Layers:
	-	`sha256:bddb34d1441457ba197ed211c3c999bbba9e59fb24ef8e5e7472cae7ea0a24d5`  
		Last Modified: Mon, 09 Mar 2026 21:49:45 GMT  
		Size: 6.7 MB (6669545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8590d1224fba9b1e3d2c918fad38f9c13302d21f970a8b13301f3e5611684e9`  
		Last Modified: Mon, 09 Mar 2026 21:49:45 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7addc648b5e67c67b864ab97fb7d52a29a466c27b5f7b4ad86806294394dd923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158858481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62dbc4b5dbddfba90291d7d6cba452978c82e3fedffc5d69733149cd29b8237`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 21:53:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 21:53:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Mar 2026 21:53:54 GMT
ENV TELEGRAF_VERSION=1.38.0
# Mon, 09 Mar 2026 21:53:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Mar 2026 21:53:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Mar 2026 21:53:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Mar 2026 21:53:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Mar 2026 21:53:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:510542cb38bcb0c99cf41f8715bc80ae2e63df19b8399efbb11254ee0ddd4299`  
		Last Modified: Tue, 24 Feb 2026 18:41:53 GMT  
		Size: 44.2 MB (44207818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122a79376a0d51f606a8d45c17043adef288961e7b30a2332c485fac0427d825`  
		Last Modified: Tue, 24 Feb 2026 20:01:59 GMT  
		Size: 21.9 MB (21942084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264913ff04f2b246dd3e5470ac926c608176024e34118fc01c113c74db4d4edf`  
		Last Modified: Mon, 09 Mar 2026 21:54:11 GMT  
		Size: 17.7 MB (17699698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b0d86f79a685e7431f092d15cafa67227d3e289fc5a8655edd36913b0e06cd`  
		Last Modified: Mon, 09 Mar 2026 21:54:10 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f44f673bcb705bc93d7e91ebab93e1800fd8bef8f7f904d78121d7eb8202927`  
		Last Modified: Mon, 09 Mar 2026 21:54:13 GMT  
		Size: 75.0 MB (75003186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11598bf028561cffdfcef29a9266653eb245af4e01889c99ea0d46eea6401eb5`  
		Last Modified: Mon, 09 Mar 2026 21:54:10 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:8d2a3447cad3d75d152b1f91f5c2cf7e55a28d764d19d81ca24ec325e9c1ed1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6678977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd29487f0cc5d855244171c514ad93b14e60c2c9b4706035fc476ccb52b3b234`

```dockerfile
```

-	Layers:
	-	`sha256:4d9e3000c42feb043bd756017955b27689e55c47dedaa95dd76141bb3e53045b`  
		Last Modified: Mon, 09 Mar 2026 21:54:11 GMT  
		Size: 6.7 MB (6664150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ff3b0c58ebd1a6ccf8f6415261b95df9d996f476524d06e1a47aa511e8f11e`  
		Last Modified: Mon, 09 Mar 2026 21:54:10 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:1436027c3f32491b707f0f32126da625fb6cd50502c8adec94352d5b76fb9916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163405527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93fc5674f8abe1ecf0e62fbb4274e10519686c09f03e83af604a969d6fa6d829`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 21:49:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 21:49:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Mar 2026 21:49:14 GMT
ENV TELEGRAF_VERSION=1.38.0
# Mon, 09 Mar 2026 21:49:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Mar 2026 21:49:14 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Mar 2026 21:49:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Mar 2026 21:49:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Mar 2026 21:49:14 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7499ccd4ff0930f49a9b38813f4d7464da8605372b23b0961163da2942938f25`  
		Last Modified: Mon, 09 Mar 2026 21:49:32 GMT  
		Size: 18.9 MB (18885833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506e042ffcc321652e840bc20dd7d83c360c9e93a110847aba14e5241b523969`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750ffd12261dd8cc01f1d938f30e83924a6f0e8b8748a222a023d6facab459d9`  
		Last Modified: Mon, 09 Mar 2026 21:49:34 GMT  
		Size: 72.5 MB (72536070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71127c4484bc93505e645c6552461fff86a399a266fcb6b465f6bd1911699026`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:c26591995b2ad9646c3c6ec3681c4aefcd8d7a2e3698de2ec1795f7a74f5b141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6685084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d541217d78bac5808758ea06799b94f256ab4fcefca5a196dee91f3d9f994e`

```dockerfile
```

-	Layers:
	-	`sha256:9533541ac6a641b9b74e1a7352106d31d634fa968a9756d12c32d7590a1c119f`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 6.7 MB (6670233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b63c60d826052f28678e067008a6e0037d471fd1eba0d0a7194833c8923c6c6d`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38-alpine`

```console
$ docker pull telegraf@sha256:96f24f9d67eab0a43da9f0d7d0929ab83196a94f57b547d59af293151c3c11c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c3f87c1dc8381c898c37be04a167a0296b9823485ae29afa3e4ff03a0cb10e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87331938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b59eede2f675a1f762db0a0339825209fcab763d83ea784f586f04075362c90`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 21:49:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Mar 2026 21:49:56 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 09 Mar 2026 21:50:04 GMT
ENV TELEGRAF_VERSION=1.38.0
# Mon, 09 Mar 2026 21:50:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Mar 2026 21:50:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Mar 2026 21:50:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Mar 2026 21:50:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Mar 2026 21:50:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2497eacf0fa9268cd0cfdee1375906f895808076c1df2921d05e0dab5dcf46`  
		Last Modified: Mon, 09 Mar 2026 21:50:19 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59883136fadd5cd69c704ab0950f241f47d61ee9614fa842c41e51f9eecc2c0d`  
		Last Modified: Mon, 09 Mar 2026 21:50:19 GMT  
		Size: 2.6 MB (2563394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9760ab35a881860ae68ae6b9d6bd6bba8b6de76f529749b055961a3fcfb644`  
		Last Modified: Mon, 09 Mar 2026 21:50:21 GMT  
		Size: 81.0 MB (80962769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36c3980ff33248985f95c448f5181e6a33f0d2a0239746c01ac0bf802b39135`  
		Last Modified: Mon, 09 Mar 2026 21:50:19 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:48a9ddf77250af029ea77f311be3d7cc00b11ad005cc76ebd536563987275c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1170970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba289fc87d145f380e5fbc64817ea3a709e6e69463e4429f5cae9b95ed8040c4`

```dockerfile
```

-	Layers:
	-	`sha256:0afc03cabbcc5acaaf672d574179e85c2416683fab6eb28fc8a56d8e964ad665`  
		Last Modified: Mon, 09 Mar 2026 21:50:19 GMT  
		Size: 1.2 MB (1155750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed8e3f97ca51a957a9a8f0767aabb1cd127ae32d43905ac2053b79a3dbc1dbaa`  
		Last Modified: Mon, 09 Mar 2026 21:50:19 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d6194dc6f53a772ebe11ef606b90fc81d3f15c19346225cb5ab40229f298f8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79094318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915056659a96d9b0845eb34b95b115320d80cfbaad0aeaf1a2ef2c910bdf0d15`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 21:49:40 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Mar 2026 21:49:41 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 09 Mar 2026 21:49:50 GMT
ENV TELEGRAF_VERSION=1.38.0
# Mon, 09 Mar 2026 21:49:50 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Mar 2026 21:49:50 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Mar 2026 21:49:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Mar 2026 21:49:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Mar 2026 21:49:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603be158bcc09db90a9dfa0b5ba742309af9eb6b2f00246c7c4152836a2e2e95`  
		Last Modified: Mon, 09 Mar 2026 21:50:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fdda0abe53661aa7646293de0e1325a89c6677132c24916959418600fb0896`  
		Last Modified: Mon, 09 Mar 2026 21:50:03 GMT  
		Size: 2.6 MB (2627400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8311ea834588316afa4514b6b3044a679e3331b10adaa88a80587fbefa002d9b`  
		Last Modified: Mon, 09 Mar 2026 21:50:05 GMT  
		Size: 72.3 MB (72326501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5c71668b77f15e5217ea3997a2b990116940ac3027db9d34717b920698b620`  
		Last Modified: Mon, 09 Mar 2026 21:50:03 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9c639a65531c36a56eff07ad6fbce22eeed8b2013052b0e9afd10ef06693d441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1166731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945cd728f3cf8746fb393b7583c1cd1fb04e067bf8106063cbf09c91d9813548`

```dockerfile
```

-	Layers:
	-	`sha256:2e88084ef116452c9e35014db3e1b5adf26817e89cb83531d2cfdd73a58a91d1`  
		Last Modified: Mon, 09 Mar 2026 21:50:03 GMT  
		Size: 1.2 MB (1151389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27dab7f6165a53b3d4d2f5579fd35313958b1e605f34ce34407250ada190854f`  
		Last Modified: Mon, 09 Mar 2026 21:50:03 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38.1`

```console
$ docker pull telegraf@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `telegraf:1.38.1-alpine`

```console
$ docker pull telegraf@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:96f24f9d67eab0a43da9f0d7d0929ab83196a94f57b547d59af293151c3c11c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c3f87c1dc8381c898c37be04a167a0296b9823485ae29afa3e4ff03a0cb10e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87331938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b59eede2f675a1f762db0a0339825209fcab763d83ea784f586f04075362c90`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 21:49:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Mar 2026 21:49:56 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 09 Mar 2026 21:50:04 GMT
ENV TELEGRAF_VERSION=1.38.0
# Mon, 09 Mar 2026 21:50:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Mar 2026 21:50:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Mar 2026 21:50:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Mar 2026 21:50:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Mar 2026 21:50:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2497eacf0fa9268cd0cfdee1375906f895808076c1df2921d05e0dab5dcf46`  
		Last Modified: Mon, 09 Mar 2026 21:50:19 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59883136fadd5cd69c704ab0950f241f47d61ee9614fa842c41e51f9eecc2c0d`  
		Last Modified: Mon, 09 Mar 2026 21:50:19 GMT  
		Size: 2.6 MB (2563394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9760ab35a881860ae68ae6b9d6bd6bba8b6de76f529749b055961a3fcfb644`  
		Last Modified: Mon, 09 Mar 2026 21:50:21 GMT  
		Size: 81.0 MB (80962769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36c3980ff33248985f95c448f5181e6a33f0d2a0239746c01ac0bf802b39135`  
		Last Modified: Mon, 09 Mar 2026 21:50:19 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:48a9ddf77250af029ea77f311be3d7cc00b11ad005cc76ebd536563987275c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1170970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba289fc87d145f380e5fbc64817ea3a709e6e69463e4429f5cae9b95ed8040c4`

```dockerfile
```

-	Layers:
	-	`sha256:0afc03cabbcc5acaaf672d574179e85c2416683fab6eb28fc8a56d8e964ad665`  
		Last Modified: Mon, 09 Mar 2026 21:50:19 GMT  
		Size: 1.2 MB (1155750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed8e3f97ca51a957a9a8f0767aabb1cd127ae32d43905ac2053b79a3dbc1dbaa`  
		Last Modified: Mon, 09 Mar 2026 21:50:19 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d6194dc6f53a772ebe11ef606b90fc81d3f15c19346225cb5ab40229f298f8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79094318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915056659a96d9b0845eb34b95b115320d80cfbaad0aeaf1a2ef2c910bdf0d15`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 21:49:40 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Mar 2026 21:49:41 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 09 Mar 2026 21:49:50 GMT
ENV TELEGRAF_VERSION=1.38.0
# Mon, 09 Mar 2026 21:49:50 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Mar 2026 21:49:50 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Mar 2026 21:49:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Mar 2026 21:49:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Mar 2026 21:49:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603be158bcc09db90a9dfa0b5ba742309af9eb6b2f00246c7c4152836a2e2e95`  
		Last Modified: Mon, 09 Mar 2026 21:50:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fdda0abe53661aa7646293de0e1325a89c6677132c24916959418600fb0896`  
		Last Modified: Mon, 09 Mar 2026 21:50:03 GMT  
		Size: 2.6 MB (2627400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8311ea834588316afa4514b6b3044a679e3331b10adaa88a80587fbefa002d9b`  
		Last Modified: Mon, 09 Mar 2026 21:50:05 GMT  
		Size: 72.3 MB (72326501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5c71668b77f15e5217ea3997a2b990116940ac3027db9d34717b920698b620`  
		Last Modified: Mon, 09 Mar 2026 21:50:03 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9c639a65531c36a56eff07ad6fbce22eeed8b2013052b0e9afd10ef06693d441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1166731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945cd728f3cf8746fb393b7583c1cd1fb04e067bf8106063cbf09c91d9813548`

```dockerfile
```

-	Layers:
	-	`sha256:2e88084ef116452c9e35014db3e1b5adf26817e89cb83531d2cfdd73a58a91d1`  
		Last Modified: Mon, 09 Mar 2026 21:50:03 GMT  
		Size: 1.2 MB (1151389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27dab7f6165a53b3d4d2f5579fd35313958b1e605f34ce34407250ada190854f`  
		Last Modified: Mon, 09 Mar 2026 21:50:03 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:b7c11b83c594a660d89ff86e745405035734fc33857bbadde550d07f8452629b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:24a87b4118d623e434000bbf0e8c77b3e4d1bcb9d45747728c94d40f6d2e0016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172649887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c517bb8ced7edf8a7cc3b1e703dc9ac1c18b92675999bfb37ded301ac90f862`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 21:49:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 21:49:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Mar 2026 21:49:28 GMT
ENV TELEGRAF_VERSION=1.38.0
# Mon, 09 Mar 2026 21:49:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Mar 2026 21:49:28 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Mar 2026 21:49:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Mar 2026 21:49:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Mar 2026 21:49:28 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c50ce151bfa926c59b4224aadf63a506b9f97bd82366e3527cc332b7b291b30`  
		Last Modified: Mon, 09 Mar 2026 21:49:46 GMT  
		Size: 18.9 MB (18944455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434659474c2b3d691943ef0eb09fda91f8b28d10db480ebe4d907e3b68b68365`  
		Last Modified: Mon, 09 Mar 2026 21:49:45 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1965c1cf786e3766ad23e21994fec7ceaff39e245491620b59eb686fb9d51a79`  
		Last Modified: Mon, 09 Mar 2026 21:49:48 GMT  
		Size: 81.2 MB (81172510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1e3c216f806b640485ca8ff1cba0d4d0150ae736435b92f82ceb6c5bf7f77e`  
		Last Modified: Mon, 09 Mar 2026 21:49:45 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:5816d7a55657ecd2dd95064da98a5381ef1b27a510e91eb41fbe06e5f5f7ff4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af52e79e49a3062640b3a36deba37a4d006311f3c340d0d791ae406562f39d6b`

```dockerfile
```

-	Layers:
	-	`sha256:bddb34d1441457ba197ed211c3c999bbba9e59fb24ef8e5e7472cae7ea0a24d5`  
		Last Modified: Mon, 09 Mar 2026 21:49:45 GMT  
		Size: 6.7 MB (6669545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8590d1224fba9b1e3d2c918fad38f9c13302d21f970a8b13301f3e5611684e9`  
		Last Modified: Mon, 09 Mar 2026 21:49:45 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7addc648b5e67c67b864ab97fb7d52a29a466c27b5f7b4ad86806294394dd923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158858481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62dbc4b5dbddfba90291d7d6cba452978c82e3fedffc5d69733149cd29b8237`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 21:53:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 21:53:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Mar 2026 21:53:54 GMT
ENV TELEGRAF_VERSION=1.38.0
# Mon, 09 Mar 2026 21:53:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Mar 2026 21:53:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Mar 2026 21:53:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Mar 2026 21:53:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Mar 2026 21:53:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:510542cb38bcb0c99cf41f8715bc80ae2e63df19b8399efbb11254ee0ddd4299`  
		Last Modified: Tue, 24 Feb 2026 18:41:53 GMT  
		Size: 44.2 MB (44207818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122a79376a0d51f606a8d45c17043adef288961e7b30a2332c485fac0427d825`  
		Last Modified: Tue, 24 Feb 2026 20:01:59 GMT  
		Size: 21.9 MB (21942084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264913ff04f2b246dd3e5470ac926c608176024e34118fc01c113c74db4d4edf`  
		Last Modified: Mon, 09 Mar 2026 21:54:11 GMT  
		Size: 17.7 MB (17699698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b0d86f79a685e7431f092d15cafa67227d3e289fc5a8655edd36913b0e06cd`  
		Last Modified: Mon, 09 Mar 2026 21:54:10 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f44f673bcb705bc93d7e91ebab93e1800fd8bef8f7f904d78121d7eb8202927`  
		Last Modified: Mon, 09 Mar 2026 21:54:13 GMT  
		Size: 75.0 MB (75003186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11598bf028561cffdfcef29a9266653eb245af4e01889c99ea0d46eea6401eb5`  
		Last Modified: Mon, 09 Mar 2026 21:54:10 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:8d2a3447cad3d75d152b1f91f5c2cf7e55a28d764d19d81ca24ec325e9c1ed1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6678977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd29487f0cc5d855244171c514ad93b14e60c2c9b4706035fc476ccb52b3b234`

```dockerfile
```

-	Layers:
	-	`sha256:4d9e3000c42feb043bd756017955b27689e55c47dedaa95dd76141bb3e53045b`  
		Last Modified: Mon, 09 Mar 2026 21:54:11 GMT  
		Size: 6.7 MB (6664150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ff3b0c58ebd1a6ccf8f6415261b95df9d996f476524d06e1a47aa511e8f11e`  
		Last Modified: Mon, 09 Mar 2026 21:54:10 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:1436027c3f32491b707f0f32126da625fb6cd50502c8adec94352d5b76fb9916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163405527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93fc5674f8abe1ecf0e62fbb4274e10519686c09f03e83af604a969d6fa6d829`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 21:49:07 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 21:49:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Mar 2026 21:49:14 GMT
ENV TELEGRAF_VERSION=1.38.0
# Mon, 09 Mar 2026 21:49:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Mar 2026 21:49:14 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Mar 2026 21:49:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Mar 2026 21:49:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Mar 2026 21:49:14 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7499ccd4ff0930f49a9b38813f4d7464da8605372b23b0961163da2942938f25`  
		Last Modified: Mon, 09 Mar 2026 21:49:32 GMT  
		Size: 18.9 MB (18885833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506e042ffcc321652e840bc20dd7d83c360c9e93a110847aba14e5241b523969`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750ffd12261dd8cc01f1d938f30e83924a6f0e8b8748a222a023d6facab459d9`  
		Last Modified: Mon, 09 Mar 2026 21:49:34 GMT  
		Size: 72.5 MB (72536070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71127c4484bc93505e645c6552461fff86a399a266fcb6b465f6bd1911699026`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:c26591995b2ad9646c3c6ec3681c4aefcd8d7a2e3698de2ec1795f7a74f5b141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6685084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d541217d78bac5808758ea06799b94f256ab4fcefca5a196dee91f3d9f994e`

```dockerfile
```

-	Layers:
	-	`sha256:9533541ac6a641b9b74e1a7352106d31d634fa968a9756d12c32d7590a1c119f`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 6.7 MB (6670233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b63c60d826052f28678e067008a6e0037d471fd1eba0d0a7194833c8923c6c6d`  
		Last Modified: Mon, 09 Mar 2026 21:49:31 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
