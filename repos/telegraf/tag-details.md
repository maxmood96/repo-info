<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.37`](#telegraf137)
-	[`telegraf:1.37-alpine`](#telegraf137-alpine)
-	[`telegraf:1.37.3`](#telegraf1373)
-	[`telegraf:1.37.3-alpine`](#telegraf1373-alpine)
-	[`telegraf:1.38`](#telegraf138)
-	[`telegraf:1.38-alpine`](#telegraf138-alpine)
-	[`telegraf:1.38.4`](#telegraf1384)
-	[`telegraf:1.38.4-alpine`](#telegraf1384-alpine)
-	[`telegraf:1.39`](#telegraf139)
-	[`telegraf:1.39-alpine`](#telegraf139-alpine)
-	[`telegraf:1.39.0`](#telegraf1390)
-	[`telegraf:1.39.0-alpine`](#telegraf1390-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.37`

```console
$ docker pull telegraf@sha256:59d829e7ed5a022ab7792abcec71f5736866d7df636fe68527d011974db1edaf
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
$ docker pull telegraf@sha256:9d807a8128bb0b7c890d2cd5c2e8a6df6d9537159a17ed4b9c33d01d52264489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172272119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8d148261f07bfa4fe882a5e1d5d3352da21fda5b24ad78e7e5e9f2021c29cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:38:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:38:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:39:01 GMT
ENV TELEGRAF_VERSION=1.37.3
# Wed, 20 May 2026 00:39:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 20 May 2026 00:39:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 20 May 2026 00:39:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:39:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:39:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52f0cfae13e87f22cf20e795b0f12fb0248d879b9a47418fd5f31ca21749380`  
		Last Modified: Wed, 20 May 2026 00:39:19 GMT  
		Size: 18.9 MB (18944430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd1b267e9b0aced4c0b71e398d9bac23460ecdb961af022362e34484f3441b9`  
		Last Modified: Wed, 20 May 2026 00:39:17 GMT  
		Size: 5.1 KB (5068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd428c3e6423c207e46917b2d729f0b0711ad361faf159f1f37e63c28e29958`  
		Last Modified: Wed, 20 May 2026 00:39:20 GMT  
		Size: 80.8 MB (80783190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b4c98833bc25a18951a9d54f9e25de84e3b99c47e09a601b645fa57f0da0ae`  
		Last Modified: Wed, 20 May 2026 00:39:18 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:d8758846a78ac66f987d6fbae8751b93ada0e06e53a27292905e88a02bdf5b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2bb1b7e90479a1e3728d18b66fa3ee13ac9e8d71371f9690613901f1428adc`

```dockerfile
```

-	Layers:
	-	`sha256:a3c6206ffc782f7154839fdf6199ec46eef38489cf3d7b31a32be8cf625ed4c5`  
		Last Modified: Wed, 20 May 2026 00:39:18 GMT  
		Size: 6.7 MB (6666976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d40e79a681e64f6af16d0902539e4f995de0ffafc3f72e2cc02b28a841bee98`  
		Last Modified: Wed, 20 May 2026 00:39:17 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:de369692084af412a7299ed443d1c703582a10778f3b97c32c7f884e22b10aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158482077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596f4abc4981b70a240e7f81093e99b410b743d8d38ddca0a22dd69261395d25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:46:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:46:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 01:46:43 GMT
ENV TELEGRAF_VERSION=1.37.3
# Wed, 20 May 2026 01:46:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 20 May 2026 01:46:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 20 May 2026 01:46:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 01:46:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 01:46:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61246c0a5a0fe9fe8cdc1bfde0fdfa49ffafcc94cba31f4aecc0c34bc346064`  
		Last Modified: Wed, 20 May 2026 00:02:11 GMT  
		Size: 22.0 MB (21950133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4998c3d3af940b149cb85b5f357ba524fdc26efef89ac693a0937c1429d4e12`  
		Last Modified: Wed, 20 May 2026 01:47:01 GMT  
		Size: 17.7 MB (17699594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22e838ea17f39c4bef9d95a34a435991ba82b8d2137bf9d2dce8f3352bc79d9`  
		Last Modified: Wed, 20 May 2026 01:46:59 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12fff064b75974b9ba4817791184475d349b2089fc6cff6a20fc4968d4ecfc6`  
		Last Modified: Wed, 20 May 2026 01:47:02 GMT  
		Size: 74.6 MB (74617502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8327f282eaab00900bd1aa8b9a453cabdb2e831f65830e708a4276b52699c1ff`  
		Last Modified: Wed, 20 May 2026 01:47:00 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:ff7288de715a2741712af3015d941476bc6f40b9a617b70b3cc53168a9421eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cf1c5cf69e693128617e93065987a47ad32f801cea18445063a421e4cf68f8`

```dockerfile
```

-	Layers:
	-	`sha256:d72ca116257e256f50133dfeb48eeb72b08aab8c8ea81c7194f893f4ee3a14f4`  
		Last Modified: Wed, 20 May 2026 01:47:00 GMT  
		Size: 6.7 MB (6661573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a849669a415a372427600bd06f64ccdd688900d674a12dfed914d68f31f2db`  
		Last Modified: Wed, 20 May 2026 01:47:00 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f4fab5371fe8e55b12b11618bc89c085e744e8f1150630b5b8dfd858dfdcaa7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163055256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef313a6eda576423e2c65dc314a464082d299bf82e29edad1d29e22e6e64030`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:40:48 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:40:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:40:53 GMT
ENV TELEGRAF_VERSION=1.37.3
# Wed, 20 May 2026 00:40:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 20 May 2026 00:40:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 20 May 2026 00:40:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:40:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:40:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d2f93710d08854b3fecbc6aabc8c44a9a120096427a74cf7334ce44ca5a2a8`  
		Last Modified: Wed, 20 May 2026 00:41:12 GMT  
		Size: 18.9 MB (18885748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c039bf5ec8afaa8386184538699456f0765ed3162333e85c4ef05e8841b244`  
		Last Modified: Wed, 20 May 2026 00:41:11 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c1960d61bcb4ac6a12b27342e5d5eb02f0775e483c489b9f8d6308df21d7bb`  
		Last Modified: Wed, 20 May 2026 00:41:13 GMT  
		Size: 72.2 MB (72171004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c849b4c91224003a644a54246963dfb32376896c88503b2d30b8e77f71b40f`  
		Last Modified: Wed, 20 May 2026 00:41:11 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:d2df6fbeca7774e8b4ac0ca07ef8dfac0d76b6e675ee12c208348cf956f6a94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cee2856e84e9635d87f883a205fd4f9a90f96e08995317d000b24d1f7ed29fe`

```dockerfile
```

-	Layers:
	-	`sha256:f37fc5893090895f80695bdb4290909e768ce9ac37c86e040faa7a4a91df9463`  
		Last Modified: Wed, 20 May 2026 00:41:11 GMT  
		Size: 6.7 MB (6667652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10d378a6737f962415233cdf9fc429825a234662f6000152823fe37873df2beb`  
		Last Modified: Wed, 20 May 2026 00:41:11 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37-alpine`

```console
$ docker pull telegraf@sha256:7ce48bd5c31b4445f9374372e878e4eaaa0fe9a1a09038e48fbe2ffdcf3688c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:8dc34975014acbe34d8f1c9840a68e3c22a91a756badd81dbcef76581390d9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86947908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d5b66113f71a03ab0425b955c1deb5ba3f0c77b95c2b51ae1b4671c7b79d86`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:35:17 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:35:26 GMT
ENV TELEGRAF_VERSION=1.37.3
# Fri, 17 Apr 2026 00:35:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Fri, 17 Apr 2026 00:35:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 17 Apr 2026 00:35:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:35:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:35:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7600c85c12c2ddea00a9ffd598e19d68011c93d7ff61b76b12d615b618d996`  
		Last Modified: Fri, 17 Apr 2026 00:30:27 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a51d3715d3b0601ef9268636e1023122bea6ae3bb0fafbfe706893c084c2b8`  
		Last Modified: Fri, 17 Apr 2026 00:35:40 GMT  
		Size: 2.6 MB (2562092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71083104bc01e56e9de463fdb3005eaa1893af5c4a695e3d2162ad2bd3ef1db6`  
		Last Modified: Fri, 17 Apr 2026 00:35:42 GMT  
		Size: 80.6 MB (80576729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72681e60733a7583a520d23d4d887a797429e5fa0224a8f37563965788a2b361`  
		Last Modified: Fri, 17 Apr 2026 00:35:40 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:72fda82e1ce6efbf9c5daf84534c21fa25028de4f94bae3085f53abb68bd61bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1167394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f681817e17e1c087aee4b058ddef6e464bef59279a5c91f9df01e38830bd3d45`

```dockerfile
```

-	Layers:
	-	`sha256:3fe66e1a1733c82f9e247d838f0a2bef9f271cc994740be8089bc39bab296490`  
		Last Modified: Fri, 17 Apr 2026 00:35:40 GMT  
		Size: 1.2 MB (1152476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e4d2627591f9d25cc99ea260d322b98694609da032c6ae21d328f1d37a2e656`  
		Last Modified: Fri, 17 Apr 2026 00:35:40 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:18045c4777e9e64159571af8098a783ea888a90d8b92b970580907f2d973855a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78732054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7589f8514fb411ea5b8fb73b4536c12c8c79043b1302c67562edc3fb1a2bc9cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:39:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:39:17 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:39:26 GMT
ENV TELEGRAF_VERSION=1.37.3
# Fri, 17 Apr 2026 00:39:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Fri, 17 Apr 2026 00:39:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 17 Apr 2026 00:39:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:39:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:39:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96f22d1f5699a3326a5b940499fa9fe7b7357964fae6531d8af1885eb09358a`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37cbdd61b2cd6abaa0b31912f17c681f202f7cc6c15bc6e0c37ab9268b785ba`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 2.6 MB (2626894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e0cbb4f736f59179413e8cafe912549e9a33cde6e1f56eb9193f499f86d7bc`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 72.0 MB (71962368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1cfc5c288d01b4e69a072c6f493dcc7bd2ca7bcec8978c66386e943337ca9d`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d9cb24d71eaa220f09fbec2e28f039f46ee85a7fd3cfd837e6f639a848af49b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1163130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6051285162d488c6150940d19ff88ddb0bca537ac70a6451d6a0c355722fc5`

```dockerfile
```

-	Layers:
	-	`sha256:eefa7a071bcab8d81979b369b4a1d7d163c82d6da0847b977a1bc31c1474ac09`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 1.1 MB (1148103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32fcbca9fdcfe9317c201f860fd3e6f9318a9055e2bac9e7aed6297bd5ba98d4`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 15.0 KB (15027 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.3`

```console
$ docker pull telegraf@sha256:59d829e7ed5a022ab7792abcec71f5736866d7df636fe68527d011974db1edaf
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
$ docker pull telegraf@sha256:9d807a8128bb0b7c890d2cd5c2e8a6df6d9537159a17ed4b9c33d01d52264489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172272119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8d148261f07bfa4fe882a5e1d5d3352da21fda5b24ad78e7e5e9f2021c29cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:38:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:38:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:39:01 GMT
ENV TELEGRAF_VERSION=1.37.3
# Wed, 20 May 2026 00:39:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 20 May 2026 00:39:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 20 May 2026 00:39:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:39:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:39:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52f0cfae13e87f22cf20e795b0f12fb0248d879b9a47418fd5f31ca21749380`  
		Last Modified: Wed, 20 May 2026 00:39:19 GMT  
		Size: 18.9 MB (18944430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd1b267e9b0aced4c0b71e398d9bac23460ecdb961af022362e34484f3441b9`  
		Last Modified: Wed, 20 May 2026 00:39:17 GMT  
		Size: 5.1 KB (5068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd428c3e6423c207e46917b2d729f0b0711ad361faf159f1f37e63c28e29958`  
		Last Modified: Wed, 20 May 2026 00:39:20 GMT  
		Size: 80.8 MB (80783190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b4c98833bc25a18951a9d54f9e25de84e3b99c47e09a601b645fa57f0da0ae`  
		Last Modified: Wed, 20 May 2026 00:39:18 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:d8758846a78ac66f987d6fbae8751b93ada0e06e53a27292905e88a02bdf5b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2bb1b7e90479a1e3728d18b66fa3ee13ac9e8d71371f9690613901f1428adc`

```dockerfile
```

-	Layers:
	-	`sha256:a3c6206ffc782f7154839fdf6199ec46eef38489cf3d7b31a32be8cf625ed4c5`  
		Last Modified: Wed, 20 May 2026 00:39:18 GMT  
		Size: 6.7 MB (6666976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d40e79a681e64f6af16d0902539e4f995de0ffafc3f72e2cc02b28a841bee98`  
		Last Modified: Wed, 20 May 2026 00:39:17 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:de369692084af412a7299ed443d1c703582a10778f3b97c32c7f884e22b10aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158482077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596f4abc4981b70a240e7f81093e99b410b743d8d38ddca0a22dd69261395d25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:46:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:46:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 01:46:43 GMT
ENV TELEGRAF_VERSION=1.37.3
# Wed, 20 May 2026 01:46:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 20 May 2026 01:46:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 20 May 2026 01:46:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 01:46:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 01:46:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61246c0a5a0fe9fe8cdc1bfde0fdfa49ffafcc94cba31f4aecc0c34bc346064`  
		Last Modified: Wed, 20 May 2026 00:02:11 GMT  
		Size: 22.0 MB (21950133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4998c3d3af940b149cb85b5f357ba524fdc26efef89ac693a0937c1429d4e12`  
		Last Modified: Wed, 20 May 2026 01:47:01 GMT  
		Size: 17.7 MB (17699594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22e838ea17f39c4bef9d95a34a435991ba82b8d2137bf9d2dce8f3352bc79d9`  
		Last Modified: Wed, 20 May 2026 01:46:59 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12fff064b75974b9ba4817791184475d349b2089fc6cff6a20fc4968d4ecfc6`  
		Last Modified: Wed, 20 May 2026 01:47:02 GMT  
		Size: 74.6 MB (74617502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8327f282eaab00900bd1aa8b9a453cabdb2e831f65830e708a4276b52699c1ff`  
		Last Modified: Wed, 20 May 2026 01:47:00 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:ff7288de715a2741712af3015d941476bc6f40b9a617b70b3cc53168a9421eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cf1c5cf69e693128617e93065987a47ad32f801cea18445063a421e4cf68f8`

```dockerfile
```

-	Layers:
	-	`sha256:d72ca116257e256f50133dfeb48eeb72b08aab8c8ea81c7194f893f4ee3a14f4`  
		Last Modified: Wed, 20 May 2026 01:47:00 GMT  
		Size: 6.7 MB (6661573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a849669a415a372427600bd06f64ccdd688900d674a12dfed914d68f31f2db`  
		Last Modified: Wed, 20 May 2026 01:47:00 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f4fab5371fe8e55b12b11618bc89c085e744e8f1150630b5b8dfd858dfdcaa7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163055256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef313a6eda576423e2c65dc314a464082d299bf82e29edad1d29e22e6e64030`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:40:48 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:40:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:40:53 GMT
ENV TELEGRAF_VERSION=1.37.3
# Wed, 20 May 2026 00:40:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 20 May 2026 00:40:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 20 May 2026 00:40:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:40:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:40:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d2f93710d08854b3fecbc6aabc8c44a9a120096427a74cf7334ce44ca5a2a8`  
		Last Modified: Wed, 20 May 2026 00:41:12 GMT  
		Size: 18.9 MB (18885748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c039bf5ec8afaa8386184538699456f0765ed3162333e85c4ef05e8841b244`  
		Last Modified: Wed, 20 May 2026 00:41:11 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c1960d61bcb4ac6a12b27342e5d5eb02f0775e483c489b9f8d6308df21d7bb`  
		Last Modified: Wed, 20 May 2026 00:41:13 GMT  
		Size: 72.2 MB (72171004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c849b4c91224003a644a54246963dfb32376896c88503b2d30b8e77f71b40f`  
		Last Modified: Wed, 20 May 2026 00:41:11 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:d2df6fbeca7774e8b4ac0ca07ef8dfac0d76b6e675ee12c208348cf956f6a94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cee2856e84e9635d87f883a205fd4f9a90f96e08995317d000b24d1f7ed29fe`

```dockerfile
```

-	Layers:
	-	`sha256:f37fc5893090895f80695bdb4290909e768ce9ac37c86e040faa7a4a91df9463`  
		Last Modified: Wed, 20 May 2026 00:41:11 GMT  
		Size: 6.7 MB (6667652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10d378a6737f962415233cdf9fc429825a234662f6000152823fe37873df2beb`  
		Last Modified: Wed, 20 May 2026 00:41:11 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.3-alpine`

```console
$ docker pull telegraf@sha256:7ce48bd5c31b4445f9374372e878e4eaaa0fe9a1a09038e48fbe2ffdcf3688c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:8dc34975014acbe34d8f1c9840a68e3c22a91a756badd81dbcef76581390d9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86947908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d5b66113f71a03ab0425b955c1deb5ba3f0c77b95c2b51ae1b4671c7b79d86`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:35:17 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:35:26 GMT
ENV TELEGRAF_VERSION=1.37.3
# Fri, 17 Apr 2026 00:35:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Fri, 17 Apr 2026 00:35:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 17 Apr 2026 00:35:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:35:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:35:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7600c85c12c2ddea00a9ffd598e19d68011c93d7ff61b76b12d615b618d996`  
		Last Modified: Fri, 17 Apr 2026 00:30:27 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a51d3715d3b0601ef9268636e1023122bea6ae3bb0fafbfe706893c084c2b8`  
		Last Modified: Fri, 17 Apr 2026 00:35:40 GMT  
		Size: 2.6 MB (2562092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71083104bc01e56e9de463fdb3005eaa1893af5c4a695e3d2162ad2bd3ef1db6`  
		Last Modified: Fri, 17 Apr 2026 00:35:42 GMT  
		Size: 80.6 MB (80576729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72681e60733a7583a520d23d4d887a797429e5fa0224a8f37563965788a2b361`  
		Last Modified: Fri, 17 Apr 2026 00:35:40 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:72fda82e1ce6efbf9c5daf84534c21fa25028de4f94bae3085f53abb68bd61bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1167394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f681817e17e1c087aee4b058ddef6e464bef59279a5c91f9df01e38830bd3d45`

```dockerfile
```

-	Layers:
	-	`sha256:3fe66e1a1733c82f9e247d838f0a2bef9f271cc994740be8089bc39bab296490`  
		Last Modified: Fri, 17 Apr 2026 00:35:40 GMT  
		Size: 1.2 MB (1152476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e4d2627591f9d25cc99ea260d322b98694609da032c6ae21d328f1d37a2e656`  
		Last Modified: Fri, 17 Apr 2026 00:35:40 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:18045c4777e9e64159571af8098a783ea888a90d8b92b970580907f2d973855a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78732054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7589f8514fb411ea5b8fb73b4536c12c8c79043b1302c67562edc3fb1a2bc9cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:39:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:39:17 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:39:26 GMT
ENV TELEGRAF_VERSION=1.37.3
# Fri, 17 Apr 2026 00:39:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Fri, 17 Apr 2026 00:39:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 17 Apr 2026 00:39:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:39:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:39:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96f22d1f5699a3326a5b940499fa9fe7b7357964fae6531d8af1885eb09358a`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37cbdd61b2cd6abaa0b31912f17c681f202f7cc6c15bc6e0c37ab9268b785ba`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 2.6 MB (2626894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e0cbb4f736f59179413e8cafe912549e9a33cde6e1f56eb9193f499f86d7bc`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 72.0 MB (71962368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1cfc5c288d01b4e69a072c6f493dcc7bd2ca7bcec8978c66386e943337ca9d`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d9cb24d71eaa220f09fbec2e28f039f46ee85a7fd3cfd837e6f639a848af49b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1163130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6051285162d488c6150940d19ff88ddb0bca537ac70a6451d6a0c355722fc5`

```dockerfile
```

-	Layers:
	-	`sha256:eefa7a071bcab8d81979b369b4a1d7d163c82d6da0847b977a1bc31c1474ac09`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 1.1 MB (1148103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32fcbca9fdcfe9317c201f860fd3e6f9318a9055e2bac9e7aed6297bd5ba98d4`  
		Last Modified: Fri, 17 Apr 2026 00:39:39 GMT  
		Size: 15.0 KB (15027 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38`

```console
$ docker pull telegraf@sha256:fb0a95f7a42958b1e7219faf075552795f7e043432a28c54baf070442b6259ee
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
$ docker pull telegraf@sha256:a82a1513350abb1c00c0bd14a8344708b56df1bcb9f6e07348d852a25f1d382c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (174999935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a332850880e7a8333cfb0b74de00d6744b29b12e10e27e5bdbeb1478a74ba0b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:39:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:39:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:39:06 GMT
ENV TELEGRAF_VERSION=1.38.4
# Wed, 20 May 2026 00:39:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 20 May 2026 00:39:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 20 May 2026 00:39:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:39:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:39:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262f4d30bced96c3ab5f025ce56eb438ea55bc017e432e16f52c37c00e9f0d9f`  
		Last Modified: Wed, 20 May 2026 00:39:26 GMT  
		Size: 18.9 MB (18944353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc812a7e226dd45f5a9288bf870c5afe784aeed10b7bb438093a1e0e6d8c54d`  
		Last Modified: Wed, 20 May 2026 00:39:25 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cae505c7a2e33eeeebd5e96dbdbb28ee56c9db4f2c9600ed0bbdc39b9d86af0`  
		Last Modified: Wed, 20 May 2026 00:39:28 GMT  
		Size: 83.5 MB (83511082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047693bea5bd92269f854ac69c8928d7d7fb6de2185e043adb5a4cbaba43eec8`  
		Last Modified: Wed, 20 May 2026 00:39:25 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:7f92e8a9320bcd6291f42192a8ae81901ff8873600ecf25382b1c4656b34cfc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6689312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5fcf55947f5746e86fdb703816425fcce1631b3ae4941e4689a19f0f04f186`

```dockerfile
```

-	Layers:
	-	`sha256:819a62e132856673d62f2ae7d37e24b8a29f186a69dca3780383e753b60ef81c`  
		Last Modified: Wed, 20 May 2026 00:39:25 GMT  
		Size: 6.7 MB (6674583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b9a652416ecb439fd881bc1a359266ece58b3ad6137914d7e2808c155e1a136`  
		Last Modified: Wed, 20 May 2026 00:39:25 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:07efa659c079d4c9943ff648642b91e78f59ea97033344fa7aa66c0455b5a775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161292585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f9f10d80e2b6c5b34662d466df5df504e51a7e6efd801626bc64c09ae727b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:46:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:46:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 01:46:46 GMT
ENV TELEGRAF_VERSION=1.38.4
# Wed, 20 May 2026 01:46:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 20 May 2026 01:46:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 20 May 2026 01:46:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 01:46:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 01:46:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61246c0a5a0fe9fe8cdc1bfde0fdfa49ffafcc94cba31f4aecc0c34bc346064`  
		Last Modified: Wed, 20 May 2026 00:02:11 GMT  
		Size: 22.0 MB (21950133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca4eee7f25cd54245b4e70cb43ccdc8cf464cb8820d3e9bac05a2492e0817e0`  
		Last Modified: Wed, 20 May 2026 01:47:05 GMT  
		Size: 17.7 MB (17699709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a980b0e2df8ee33765f5df04291d708c696661126237c8967fc0b4816f7c650`  
		Last Modified: Wed, 20 May 2026 01:47:05 GMT  
		Size: 5.1 KB (5068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c6b201437b9e75c48613c63b169c95d3f5a1481f62d902dad1cba11696a638`  
		Last Modified: Wed, 20 May 2026 01:47:07 GMT  
		Size: 77.4 MB (77427900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26c2218f05f003d938a8f0b53dc2ebc1ca4e0bc5e7cb468590e7c0a063841d8`  
		Last Modified: Wed, 20 May 2026 01:47:05 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:a7cbba2264587bc88f4091a7662693bd953d2224ca1a6c07724f2286505d05d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a199a383d5671cdd5694bd908ecd4da41521b6aacf0ed1d3b22f7b65f40a69b`

```dockerfile
```

-	Layers:
	-	`sha256:aadd75fa4eacf14b8c1105a9ec227f26d09cc6a0faf944ad4312fa17ba28361a`  
		Last Modified: Wed, 20 May 2026 01:47:05 GMT  
		Size: 6.7 MB (6669188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc902db08cc1320eb0a702606517c6b0130b111767a9eab0ce6c030ee97ed60`  
		Last Modified: Wed, 20 May 2026 01:47:05 GMT  
		Size: 14.8 KB (14826 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b701b1e13950d8f9adb53066f63432ed67662de69a4c6f45cb2e814f4566e7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165361181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db91532e2304fc092c7ce07e5aad20f305ec392acb4cbceb05dde5fdd6e79bb7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:41:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:41:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:41:05 GMT
ENV TELEGRAF_VERSION=1.38.4
# Wed, 20 May 2026 00:41:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 20 May 2026 00:41:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 20 May 2026 00:41:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:41:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:41:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b0db6fe1f2805539a2c29b2be8827946ac0cc6de09bde559a1626d9c21028`  
		Last Modified: Wed, 20 May 2026 00:41:25 GMT  
		Size: 18.9 MB (18885919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606071820b024c6f1f9751ec5becffbb43d32bba0a21d6615b6f98dc3bafc70d`  
		Last Modified: Wed, 20 May 2026 00:41:23 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f36a226b196a8456634158533c07328112710593194b8b4e70eb4e9aba6a44`  
		Last Modified: Wed, 20 May 2026 00:41:27 GMT  
		Size: 74.5 MB (74476757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b931f16d2dd094d06f4acec9c4a66c780666e0586c10b05a68605f8dc51b10`  
		Last Modified: Wed, 20 May 2026 00:41:24 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:fef566dec8821a46c8ada35b57d405b948aa940eebe7b4a8f9d7219f612e5f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db6d5363a24809490a4d5272bda10be8624d51052a0f0ab895ca767c79a3c5f`

```dockerfile
```

-	Layers:
	-	`sha256:49ee1a9ead2c3ddbbbb24b4e5d367a201ac9a37b5d5c95033ccebc5e83baa069`  
		Last Modified: Wed, 20 May 2026 00:41:24 GMT  
		Size: 6.7 MB (6675271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d0d50465488a0de90d508b1da4af5953d15ee447ab302c981e510f9038da065`  
		Last Modified: Wed, 20 May 2026 00:41:24 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38-alpine`

```console
$ docker pull telegraf@sha256:49fc4b3e60115966979d653e76874bd960acdd27cd484a4a57813132e474d882
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c7bba96a83d3784fa69230bfa127df503fc8fb40ed96579d1577695a4ebc4049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89781668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bde7e8a9f0886477eb58d149d3fdb897576a1ff2880814cec5bb3e33a87fe23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:53:34 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:53:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:53:41 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:41 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 11 May 2026 23:53:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632464fc81a2417f86866f355eb404dd6fbaf95f23753e20e4aa1e267529287c`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2019e1df3daf5a5b4b76e4c51b0f6852dfe81b1860b80f3453f1e6834f8b07e7`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 2.6 MB (2615506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55706eb6bc48155a245fd2f96c71cb107f44fcccdd2aaa7c8a9010f4d9f3531e`  
		Last Modified: Mon, 11 May 2026 23:53:59 GMT  
		Size: 83.3 MB (83301076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18d0f774411b978b4a6dcff56ac3efb4fe752d82ff76811fa2d292168e096ee`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6cfc1222edb07a0523e4a8b7d809b2cba473b87420ca92dfc9494a8e05a0249b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e4e891c501b04fc88f432dee4f0cbe8b1a2f9fbef27a8b59b5e1c8c857b410`

```dockerfile
```

-	Layers:
	-	`sha256:87172905ac106dc4e375b2ee186d37f6d4ae3e2e57f8397ed23b9df4a4af5ef3`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 1.2 MB (1159425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95634f1fdd7e204e3763697b4cc7367156ab43224e38e2c5541d394a304ed5f2`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:19af6c4fafd30c79942ce50f05f02e295c12e5b03235cdae3524693152d2297d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81139701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb01df9de16a90f3948b5ece3e32033cdede92445b135f94ab92f92ba653a91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:53:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:53:38 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:53:44 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:44 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 11 May 2026 23:53:44 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516037cb512d171e8192c72d6cce6bcc6520c5c810cd1897a55fad977b22648e`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee16394386df16ff764f3efa01797c33a2433da101aef041fd08fc6005c2cdc6`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 2.7 MB (2663399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a626a22da7deea10123bbb5b91da01956fbd43220b4895c44a51c0f606eeb453`  
		Last Modified: Mon, 11 May 2026 23:54:00 GMT  
		Size: 74.3 MB (74275535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8a4a41e5ca652cb64623bdbe2d62a7093dc0f2b34d0959c77727c15e396aea`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:2e7bcc746fce8c8515152b4009e46d0ccb46de3da94f69c8801fcc984c8309b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1169756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6a3537a13a07028d6032f354fb67501d10d8219ccc35d65313195b862e73d3`

```dockerfile
```

-	Layers:
	-	`sha256:dac57cdea5ed6e2c983aac5dd06719625adb227c4b87bc662d57a13712de8dc0`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 1.2 MB (1154414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e77d863cf01a81facd30cb97595935291e5ad1ceb3762e95f7082ff1fd5252`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38.4`

```console
$ docker pull telegraf@sha256:fb0a95f7a42958b1e7219faf075552795f7e043432a28c54baf070442b6259ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38.4` - linux; amd64

```console
$ docker pull telegraf@sha256:a82a1513350abb1c00c0bd14a8344708b56df1bcb9f6e07348d852a25f1d382c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (174999935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a332850880e7a8333cfb0b74de00d6744b29b12e10e27e5bdbeb1478a74ba0b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:39:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:39:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:39:06 GMT
ENV TELEGRAF_VERSION=1.38.4
# Wed, 20 May 2026 00:39:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 20 May 2026 00:39:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 20 May 2026 00:39:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:39:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:39:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262f4d30bced96c3ab5f025ce56eb438ea55bc017e432e16f52c37c00e9f0d9f`  
		Last Modified: Wed, 20 May 2026 00:39:26 GMT  
		Size: 18.9 MB (18944353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc812a7e226dd45f5a9288bf870c5afe784aeed10b7bb438093a1e0e6d8c54d`  
		Last Modified: Wed, 20 May 2026 00:39:25 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cae505c7a2e33eeeebd5e96dbdbb28ee56c9db4f2c9600ed0bbdc39b9d86af0`  
		Last Modified: Wed, 20 May 2026 00:39:28 GMT  
		Size: 83.5 MB (83511082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047693bea5bd92269f854ac69c8928d7d7fb6de2185e043adb5a4cbaba43eec8`  
		Last Modified: Wed, 20 May 2026 00:39:25 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:7f92e8a9320bcd6291f42192a8ae81901ff8873600ecf25382b1c4656b34cfc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6689312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5fcf55947f5746e86fdb703816425fcce1631b3ae4941e4689a19f0f04f186`

```dockerfile
```

-	Layers:
	-	`sha256:819a62e132856673d62f2ae7d37e24b8a29f186a69dca3780383e753b60ef81c`  
		Last Modified: Wed, 20 May 2026 00:39:25 GMT  
		Size: 6.7 MB (6674583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b9a652416ecb439fd881bc1a359266ece58b3ad6137914d7e2808c155e1a136`  
		Last Modified: Wed, 20 May 2026 00:39:25 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:07efa659c079d4c9943ff648642b91e78f59ea97033344fa7aa66c0455b5a775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161292585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f9f10d80e2b6c5b34662d466df5df504e51a7e6efd801626bc64c09ae727b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:46:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:46:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 01:46:46 GMT
ENV TELEGRAF_VERSION=1.38.4
# Wed, 20 May 2026 01:46:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 20 May 2026 01:46:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 20 May 2026 01:46:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 01:46:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 01:46:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61246c0a5a0fe9fe8cdc1bfde0fdfa49ffafcc94cba31f4aecc0c34bc346064`  
		Last Modified: Wed, 20 May 2026 00:02:11 GMT  
		Size: 22.0 MB (21950133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca4eee7f25cd54245b4e70cb43ccdc8cf464cb8820d3e9bac05a2492e0817e0`  
		Last Modified: Wed, 20 May 2026 01:47:05 GMT  
		Size: 17.7 MB (17699709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a980b0e2df8ee33765f5df04291d708c696661126237c8967fc0b4816f7c650`  
		Last Modified: Wed, 20 May 2026 01:47:05 GMT  
		Size: 5.1 KB (5068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c6b201437b9e75c48613c63b169c95d3f5a1481f62d902dad1cba11696a638`  
		Last Modified: Wed, 20 May 2026 01:47:07 GMT  
		Size: 77.4 MB (77427900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26c2218f05f003d938a8f0b53dc2ebc1ca4e0bc5e7cb468590e7c0a063841d8`  
		Last Modified: Wed, 20 May 2026 01:47:05 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:a7cbba2264587bc88f4091a7662693bd953d2224ca1a6c07724f2286505d05d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a199a383d5671cdd5694bd908ecd4da41521b6aacf0ed1d3b22f7b65f40a69b`

```dockerfile
```

-	Layers:
	-	`sha256:aadd75fa4eacf14b8c1105a9ec227f26d09cc6a0faf944ad4312fa17ba28361a`  
		Last Modified: Wed, 20 May 2026 01:47:05 GMT  
		Size: 6.7 MB (6669188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc902db08cc1320eb0a702606517c6b0130b111767a9eab0ce6c030ee97ed60`  
		Last Modified: Wed, 20 May 2026 01:47:05 GMT  
		Size: 14.8 KB (14826 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b701b1e13950d8f9adb53066f63432ed67662de69a4c6f45cb2e814f4566e7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165361181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db91532e2304fc092c7ce07e5aad20f305ec392acb4cbceb05dde5fdd6e79bb7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:41:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:41:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:41:05 GMT
ENV TELEGRAF_VERSION=1.38.4
# Wed, 20 May 2026 00:41:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 20 May 2026 00:41:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 20 May 2026 00:41:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:41:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:41:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b0db6fe1f2805539a2c29b2be8827946ac0cc6de09bde559a1626d9c21028`  
		Last Modified: Wed, 20 May 2026 00:41:25 GMT  
		Size: 18.9 MB (18885919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606071820b024c6f1f9751ec5becffbb43d32bba0a21d6615b6f98dc3bafc70d`  
		Last Modified: Wed, 20 May 2026 00:41:23 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f36a226b196a8456634158533c07328112710593194b8b4e70eb4e9aba6a44`  
		Last Modified: Wed, 20 May 2026 00:41:27 GMT  
		Size: 74.5 MB (74476757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b931f16d2dd094d06f4acec9c4a66c780666e0586c10b05a68605f8dc51b10`  
		Last Modified: Wed, 20 May 2026 00:41:24 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:fef566dec8821a46c8ada35b57d405b948aa940eebe7b4a8f9d7219f612e5f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db6d5363a24809490a4d5272bda10be8624d51052a0f0ab895ca767c79a3c5f`

```dockerfile
```

-	Layers:
	-	`sha256:49ee1a9ead2c3ddbbbb24b4e5d367a201ac9a37b5d5c95033ccebc5e83baa069`  
		Last Modified: Wed, 20 May 2026 00:41:24 GMT  
		Size: 6.7 MB (6675271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d0d50465488a0de90d508b1da4af5953d15ee447ab302c981e510f9038da065`  
		Last Modified: Wed, 20 May 2026 00:41:24 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38.4-alpine`

```console
$ docker pull telegraf@sha256:49fc4b3e60115966979d653e76874bd960acdd27cd484a4a57813132e474d882
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c7bba96a83d3784fa69230bfa127df503fc8fb40ed96579d1577695a4ebc4049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89781668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bde7e8a9f0886477eb58d149d3fdb897576a1ff2880814cec5bb3e33a87fe23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:53:34 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:53:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:53:41 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:41 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 11 May 2026 23:53:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632464fc81a2417f86866f355eb404dd6fbaf95f23753e20e4aa1e267529287c`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2019e1df3daf5a5b4b76e4c51b0f6852dfe81b1860b80f3453f1e6834f8b07e7`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 2.6 MB (2615506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55706eb6bc48155a245fd2f96c71cb107f44fcccdd2aaa7c8a9010f4d9f3531e`  
		Last Modified: Mon, 11 May 2026 23:53:59 GMT  
		Size: 83.3 MB (83301076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18d0f774411b978b4a6dcff56ac3efb4fe752d82ff76811fa2d292168e096ee`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6cfc1222edb07a0523e4a8b7d809b2cba473b87420ca92dfc9494a8e05a0249b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e4e891c501b04fc88f432dee4f0cbe8b1a2f9fbef27a8b59b5e1c8c857b410`

```dockerfile
```

-	Layers:
	-	`sha256:87172905ac106dc4e375b2ee186d37f6d4ae3e2e57f8397ed23b9df4a4af5ef3`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 1.2 MB (1159425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95634f1fdd7e204e3763697b4cc7367156ab43224e38e2c5541d394a304ed5f2`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:19af6c4fafd30c79942ce50f05f02e295c12e5b03235cdae3524693152d2297d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81139701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb01df9de16a90f3948b5ece3e32033cdede92445b135f94ab92f92ba653a91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:53:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:53:38 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:53:44 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:44 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 11 May 2026 23:53:44 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516037cb512d171e8192c72d6cce6bcc6520c5c810cd1897a55fad977b22648e`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee16394386df16ff764f3efa01797c33a2433da101aef041fd08fc6005c2cdc6`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 2.7 MB (2663399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a626a22da7deea10123bbb5b91da01956fbd43220b4895c44a51c0f606eeb453`  
		Last Modified: Mon, 11 May 2026 23:54:00 GMT  
		Size: 74.3 MB (74275535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8a4a41e5ca652cb64623bdbe2d62a7093dc0f2b34d0959c77727c15e396aea`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:2e7bcc746fce8c8515152b4009e46d0ccb46de3da94f69c8801fcc984c8309b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1169756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6a3537a13a07028d6032f354fb67501d10d8219ccc35d65313195b862e73d3`

```dockerfile
```

-	Layers:
	-	`sha256:dac57cdea5ed6e2c983aac5dd06719625adb227c4b87bc662d57a13712de8dc0`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 1.2 MB (1154414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e77d863cf01a81facd30cb97595935291e5ad1ceb3762e95f7082ff1fd5252`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.39`

```console
$ docker pull telegraf@sha256:1e53c1f90a46c600e330afed78500dd220586f748e2205f3ffb01bf43fd2c1e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.39` - linux; amd64

```console
$ docker pull telegraf@sha256:a2f21a5250a4fa7b7136d06b590b6bc1e0231c10508ba2592ecad73963bd5675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175311083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30be059cbbd5776d386a3d02d16643e7451afa3338a6469024d95717094f59e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 19:33:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 19:33:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Jun 2026 19:33:37 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Jun 2026 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44794ec225e2343d6440e24c585b9198e2780161b5d3f58ba9914efe1995cebd`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 18.9 MB (18944437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f0e48d45af9b728f6d794be505e7620d046e9e2bcbfc03d078f18c19ceacf5`  
		Last Modified: Mon, 08 Jun 2026 19:33:55 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38d408fc19efcf028dd8b9fb79ffc179ea241e1f22b7e7cd2cf3fc7e23846e1`  
		Last Modified: Mon, 08 Jun 2026 19:33:58 GMT  
		Size: 83.8 MB (83822147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc5b42ad8145157934895922fa932fd31f77292ab76762eeb61b7934f5b8270`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39` - unknown; unknown

```console
$ docker pull telegraf@sha256:9ee8321238f645b060ebffd167c7bb6dc56082ab62725fc81624f34c683b4df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6687648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4abcb48029b698cbfb6e90a62798f19b5ccaedb581e16e37402e59d171e332`

```dockerfile
```

-	Layers:
	-	`sha256:b7012dd76610a67176c51c48a9186507bf1911a71bb61e5fa22758f940702a79`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 6.7 MB (6672919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3d8ac59589930741af649402118e1003d6f63e5e8c41cffcf6e89db3e52843`  
		Last Modified: Mon, 08 Jun 2026 19:33:55 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.39` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:f16c74c0591b0fe89d146e33021f6a9800e26c2804d979ce49b6d443d0a393f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161566000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c8c3d3444759ad17b9c36c53a706bd2fe316a240ce0f89b2989abccfce80b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 19:31:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 19:31:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Jun 2026 19:32:02 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:32:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Jun 2026 19:32:02 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:32:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:32:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:32:02 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61246c0a5a0fe9fe8cdc1bfde0fdfa49ffafcc94cba31f4aecc0c34bc346064`  
		Last Modified: Wed, 20 May 2026 00:02:11 GMT  
		Size: 22.0 MB (21950133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358c384454c473ff91bcfedb00c1b7ee0442a1f810177b0fea490d34a7872769`  
		Last Modified: Mon, 08 Jun 2026 19:32:20 GMT  
		Size: 17.7 MB (17699712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cb18e97822996823dfd571e1e8a5421960e51d81f073e0c2aa7a0e5825c594`  
		Last Modified: Mon, 08 Jun 2026 19:32:19 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf70df52e08f905db8ad883efdf366eb8d355c181e0e5b2bdfa7b2b7fb885db`  
		Last Modified: Mon, 08 Jun 2026 19:32:21 GMT  
		Size: 77.7 MB (77701323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174cb3db59d9cf34ef1ef55526c70e41a730b3a0554245988b93e7ece5f3004f`  
		Last Modified: Mon, 08 Jun 2026 19:32:19 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39` - unknown; unknown

```console
$ docker pull telegraf@sha256:4de53eee522624492737ffb143bb59523110879a0a12cf8c2d210a9ae7964334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2951e7ff9e8f48a6ac85af50eca163949c0f2295bf735e3c350381def1238fd`

```dockerfile
```

-	Layers:
	-	`sha256:5cb4f755f4391fbd3f078e86aa02b31b873f24e82d483bf9223c7402277204fc`  
		Last Modified: Mon, 08 Jun 2026 19:32:19 GMT  
		Size: 6.7 MB (6667524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee08ebbdeb9ca500e807ce802289fc5f4aefeaa4918eadd0a6109ed4a4489d6`  
		Last Modified: Mon, 08 Jun 2026 19:32:19 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.39` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2889b1662233d9a474d3455c2de06713af5d502df3ce7c01c402d41cd3b6d937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165632766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71ad10c6f4caa1b61561669a3b82ecb28b5e29b7549902416b4b962ac38d47c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 19:33:38 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 19:33:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Jun 2026 19:33:42 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:33:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Jun 2026 19:33:42 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:33:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:33:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:33:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17ccd2326ca1cb1f4eed19ded8daa83973465368571f697b4ca8130c9f15c47`  
		Last Modified: Mon, 08 Jun 2026 19:34:01 GMT  
		Size: 18.9 MB (18885895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70342072f85a4fbd0c9c241c273928f9ad6ccce80246650009a546ecb22be8c0`  
		Last Modified: Mon, 08 Jun 2026 19:34:00 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675653bc41056bc54dff03716cdf7c3e37cd3c05f7831862511d875a7f1ad709`  
		Last Modified: Mon, 08 Jun 2026 19:34:02 GMT  
		Size: 74.7 MB (74748367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3327b896e9c815edb5df52b7761ede79230b0e8b3e041624f7847670842c8e08`  
		Last Modified: Mon, 08 Jun 2026 19:34:00 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39` - unknown; unknown

```console
$ docker pull telegraf@sha256:ad4eddb6cc3c5706747067e1b3bc53f132379432c0fc0ce2a018adae517ed912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6688458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a96932ecaa7dbeaa9ed2b403bdbec04d0edb5def1291a72d6a3754c9b19c71`

```dockerfile
```

-	Layers:
	-	`sha256:47e4180b8d72a123f8a0950239085557791d37d429960f8022f54ba5ae51c573`  
		Last Modified: Mon, 08 Jun 2026 19:34:00 GMT  
		Size: 6.7 MB (6673607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2c682bef12f5a696c03515cf70cf4658f6e91675ebbd7e7446f561287f6c0be`  
		Last Modified: Mon, 08 Jun 2026 19:34:00 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.39-alpine`

```console
$ docker pull telegraf@sha256:e5226af100b22b26b628c2f25268985541b8e04367ca1392bd704b0d488f6b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.39-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:24dfd35ff04cbaf51ee6ae2cb4adbcd0685fab04ed871d8068efefaa18b69667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90091126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3d009e134e78926811768785b2379d2553300e8a2c76c1b880293bd3c0077`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 19:33:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Jun 2026 19:33:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:33:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:33:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:33:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78cbe9dd99262d6d456db1e27c3aa45b6b06c9845c5b98cccf065f4dbd0485f`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e98f55428d3403b7d4915048651510e60b3841891394ea326d6f5238d9cdad`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 2.6 MB (2615476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eed0b000d88926bf46c7eb3555919d1b39dbab8bf2f6aa03472f49b71f917a`  
		Last Modified: Mon, 08 Jun 2026 19:33:54 GMT  
		Size: 83.6 MB (83610562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5730870d1e61bd804af545e88b2253b12266e7cb5265ef8fe4981945566b78`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4fcb5ccf45efe63c761bbd304ac29be7c49c47e184e2fcba71dfe83bb0d4e9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c0ef1b3412075ab8b75e101db7e907aee9894470f0964ac4d36214b42e7fbe`

```dockerfile
```

-	Layers:
	-	`sha256:dd82967f130f0f1255f3c9786b6d5607463a7133177fddd02d2d03f11f37ed0f`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 1.2 MB (1157761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d572b7be776dbddbbb1c26badb01d9680a53ced76feb8abf272df390138831d7`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.39-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6b66eb0080cbbf00b42b11818a220c506a9850b0c298a0fbbd50d7384a5df896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81405285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e90f2baaf68b2eba385baeab8785b6ad48c02dfa2dba818b9a6c81a9416dfa1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 19:33:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Jun 2026 19:33:41 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:33:41 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Jun 2026 19:33:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:33:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:33:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:33:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ca5dabf7783a6f9f9ce035e047cef313b5969395dd331a6ae02b4888644baf`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f722e30210b3ae00ddc7f9a8e1903197f494d3197297bc2fbf0201008bc826`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 2.7 MB (2663404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fa91218e8453a0f48f968d4e79ec2915ff4e94f9ddd205c806928bcf6401fd`  
		Last Modified: Mon, 08 Jun 2026 19:33:58 GMT  
		Size: 74.5 MB (74541112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca7bb573a3266c7638c7802e066265f0c51f4d1c3b1a8273fc32812d65618ab`  
		Last Modified: Mon, 08 Jun 2026 19:33:55 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:95293b4a78213f540b3e48a94125ce0c51a8f02593c5b9344631a30200610346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a654bf0957227d01a365840e084285d2e1ff416172a723b453027d8bd6cc77b6`

```dockerfile
```

-	Layers:
	-	`sha256:8ad6e19bd77984338905bc7bb0cff26357a4f37f952d6edf88e00b900cc3c4e0`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 1.2 MB (1152750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfff3047d82a9d84c31708e992a7106776945fa93bda13ba3af793b751c0a4f2`  
		Last Modified: Mon, 08 Jun 2026 19:33:55 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.39.0`

```console
$ docker pull telegraf@sha256:1e53c1f90a46c600e330afed78500dd220586f748e2205f3ffb01bf43fd2c1e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.39.0` - linux; amd64

```console
$ docker pull telegraf@sha256:a2f21a5250a4fa7b7136d06b590b6bc1e0231c10508ba2592ecad73963bd5675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175311083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30be059cbbd5776d386a3d02d16643e7451afa3338a6469024d95717094f59e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 19:33:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 19:33:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Jun 2026 19:33:37 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Jun 2026 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44794ec225e2343d6440e24c585b9198e2780161b5d3f58ba9914efe1995cebd`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 18.9 MB (18944437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f0e48d45af9b728f6d794be505e7620d046e9e2bcbfc03d078f18c19ceacf5`  
		Last Modified: Mon, 08 Jun 2026 19:33:55 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38d408fc19efcf028dd8b9fb79ffc179ea241e1f22b7e7cd2cf3fc7e23846e1`  
		Last Modified: Mon, 08 Jun 2026 19:33:58 GMT  
		Size: 83.8 MB (83822147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc5b42ad8145157934895922fa932fd31f77292ab76762eeb61b7934f5b8270`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:9ee8321238f645b060ebffd167c7bb6dc56082ab62725fc81624f34c683b4df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6687648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4abcb48029b698cbfb6e90a62798f19b5ccaedb581e16e37402e59d171e332`

```dockerfile
```

-	Layers:
	-	`sha256:b7012dd76610a67176c51c48a9186507bf1911a71bb61e5fa22758f940702a79`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 6.7 MB (6672919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3d8ac59589930741af649402118e1003d6f63e5e8c41cffcf6e89db3e52843`  
		Last Modified: Mon, 08 Jun 2026 19:33:55 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.39.0` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:f16c74c0591b0fe89d146e33021f6a9800e26c2804d979ce49b6d443d0a393f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161566000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c8c3d3444759ad17b9c36c53a706bd2fe316a240ce0f89b2989abccfce80b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 19:31:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 19:31:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Jun 2026 19:32:02 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:32:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Jun 2026 19:32:02 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:32:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:32:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:32:02 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61246c0a5a0fe9fe8cdc1bfde0fdfa49ffafcc94cba31f4aecc0c34bc346064`  
		Last Modified: Wed, 20 May 2026 00:02:11 GMT  
		Size: 22.0 MB (21950133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358c384454c473ff91bcfedb00c1b7ee0442a1f810177b0fea490d34a7872769`  
		Last Modified: Mon, 08 Jun 2026 19:32:20 GMT  
		Size: 17.7 MB (17699712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cb18e97822996823dfd571e1e8a5421960e51d81f073e0c2aa7a0e5825c594`  
		Last Modified: Mon, 08 Jun 2026 19:32:19 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf70df52e08f905db8ad883efdf366eb8d355c181e0e5b2bdfa7b2b7fb885db`  
		Last Modified: Mon, 08 Jun 2026 19:32:21 GMT  
		Size: 77.7 MB (77701323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174cb3db59d9cf34ef1ef55526c70e41a730b3a0554245988b93e7ece5f3004f`  
		Last Modified: Mon, 08 Jun 2026 19:32:19 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:4de53eee522624492737ffb143bb59523110879a0a12cf8c2d210a9ae7964334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2951e7ff9e8f48a6ac85af50eca163949c0f2295bf735e3c350381def1238fd`

```dockerfile
```

-	Layers:
	-	`sha256:5cb4f755f4391fbd3f078e86aa02b31b873f24e82d483bf9223c7402277204fc`  
		Last Modified: Mon, 08 Jun 2026 19:32:19 GMT  
		Size: 6.7 MB (6667524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee08ebbdeb9ca500e807ce802289fc5f4aefeaa4918eadd0a6109ed4a4489d6`  
		Last Modified: Mon, 08 Jun 2026 19:32:19 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.39.0` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2889b1662233d9a474d3455c2de06713af5d502df3ce7c01c402d41cd3b6d937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165632766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71ad10c6f4caa1b61561669a3b82ecb28b5e29b7549902416b4b962ac38d47c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 19:33:38 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 19:33:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Jun 2026 19:33:42 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:33:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Jun 2026 19:33:42 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:33:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:33:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:33:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17ccd2326ca1cb1f4eed19ded8daa83973465368571f697b4ca8130c9f15c47`  
		Last Modified: Mon, 08 Jun 2026 19:34:01 GMT  
		Size: 18.9 MB (18885895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70342072f85a4fbd0c9c241c273928f9ad6ccce80246650009a546ecb22be8c0`  
		Last Modified: Mon, 08 Jun 2026 19:34:00 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675653bc41056bc54dff03716cdf7c3e37cd3c05f7831862511d875a7f1ad709`  
		Last Modified: Mon, 08 Jun 2026 19:34:02 GMT  
		Size: 74.7 MB (74748367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3327b896e9c815edb5df52b7761ede79230b0e8b3e041624f7847670842c8e08`  
		Last Modified: Mon, 08 Jun 2026 19:34:00 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:ad4eddb6cc3c5706747067e1b3bc53f132379432c0fc0ce2a018adae517ed912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6688458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a96932ecaa7dbeaa9ed2b403bdbec04d0edb5def1291a72d6a3754c9b19c71`

```dockerfile
```

-	Layers:
	-	`sha256:47e4180b8d72a123f8a0950239085557791d37d429960f8022f54ba5ae51c573`  
		Last Modified: Mon, 08 Jun 2026 19:34:00 GMT  
		Size: 6.7 MB (6673607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2c682bef12f5a696c03515cf70cf4658f6e91675ebbd7e7446f561287f6c0be`  
		Last Modified: Mon, 08 Jun 2026 19:34:00 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.39.0-alpine`

```console
$ docker pull telegraf@sha256:e5226af100b22b26b628c2f25268985541b8e04367ca1392bd704b0d488f6b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.39.0-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:24dfd35ff04cbaf51ee6ae2cb4adbcd0685fab04ed871d8068efefaa18b69667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90091126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3d009e134e78926811768785b2379d2553300e8a2c76c1b880293bd3c0077`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 19:33:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Jun 2026 19:33:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:33:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:33:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:33:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78cbe9dd99262d6d456db1e27c3aa45b6b06c9845c5b98cccf065f4dbd0485f`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e98f55428d3403b7d4915048651510e60b3841891394ea326d6f5238d9cdad`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 2.6 MB (2615476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eed0b000d88926bf46c7eb3555919d1b39dbab8bf2f6aa03472f49b71f917a`  
		Last Modified: Mon, 08 Jun 2026 19:33:54 GMT  
		Size: 83.6 MB (83610562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5730870d1e61bd804af545e88b2253b12266e7cb5265ef8fe4981945566b78`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39.0-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4fcb5ccf45efe63c761bbd304ac29be7c49c47e184e2fcba71dfe83bb0d4e9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c0ef1b3412075ab8b75e101db7e907aee9894470f0964ac4d36214b42e7fbe`

```dockerfile
```

-	Layers:
	-	`sha256:dd82967f130f0f1255f3c9786b6d5607463a7133177fddd02d2d03f11f37ed0f`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 1.2 MB (1157761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d572b7be776dbddbbb1c26badb01d9680a53ced76feb8abf272df390138831d7`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.39.0-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6b66eb0080cbbf00b42b11818a220c506a9850b0c298a0fbbd50d7384a5df896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81405285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e90f2baaf68b2eba385baeab8785b6ad48c02dfa2dba818b9a6c81a9416dfa1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 19:33:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Jun 2026 19:33:41 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:33:41 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Jun 2026 19:33:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:33:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:33:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:33:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ca5dabf7783a6f9f9ce035e047cef313b5969395dd331a6ae02b4888644baf`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f722e30210b3ae00ddc7f9a8e1903197f494d3197297bc2fbf0201008bc826`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 2.7 MB (2663404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fa91218e8453a0f48f968d4e79ec2915ff4e94f9ddd205c806928bcf6401fd`  
		Last Modified: Mon, 08 Jun 2026 19:33:58 GMT  
		Size: 74.5 MB (74541112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca7bb573a3266c7638c7802e066265f0c51f4d1c3b1a8273fc32812d65618ab`  
		Last Modified: Mon, 08 Jun 2026 19:33:55 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.39.0-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:95293b4a78213f540b3e48a94125ce0c51a8f02593c5b9344631a30200610346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a654bf0957227d01a365840e084285d2e1ff416172a723b453027d8bd6cc77b6`

```dockerfile
```

-	Layers:
	-	`sha256:8ad6e19bd77984338905bc7bb0cff26357a4f37f952d6edf88e00b900cc3c4e0`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 1.2 MB (1152750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfff3047d82a9d84c31708e992a7106776945fa93bda13ba3af793b751c0a4f2`  
		Last Modified: Mon, 08 Jun 2026 19:33:55 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:e5226af100b22b26b628c2f25268985541b8e04367ca1392bd704b0d488f6b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:24dfd35ff04cbaf51ee6ae2cb4adbcd0685fab04ed871d8068efefaa18b69667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90091126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c3d009e134e78926811768785b2379d2553300e8a2c76c1b880293bd3c0077`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 19:33:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Jun 2026 19:33:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:33:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:33:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:33:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78cbe9dd99262d6d456db1e27c3aa45b6b06c9845c5b98cccf065f4dbd0485f`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e98f55428d3403b7d4915048651510e60b3841891394ea326d6f5238d9cdad`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 2.6 MB (2615476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eed0b000d88926bf46c7eb3555919d1b39dbab8bf2f6aa03472f49b71f917a`  
		Last Modified: Mon, 08 Jun 2026 19:33:54 GMT  
		Size: 83.6 MB (83610562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5730870d1e61bd804af545e88b2253b12266e7cb5265ef8fe4981945566b78`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4fcb5ccf45efe63c761bbd304ac29be7c49c47e184e2fcba71dfe83bb0d4e9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c0ef1b3412075ab8b75e101db7e907aee9894470f0964ac4d36214b42e7fbe`

```dockerfile
```

-	Layers:
	-	`sha256:dd82967f130f0f1255f3c9786b6d5607463a7133177fddd02d2d03f11f37ed0f`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 1.2 MB (1157761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d572b7be776dbddbbb1c26badb01d9680a53ced76feb8abf272df390138831d7`  
		Last Modified: Mon, 08 Jun 2026 19:33:51 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6b66eb0080cbbf00b42b11818a220c506a9850b0c298a0fbbd50d7384a5df896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81405285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e90f2baaf68b2eba385baeab8785b6ad48c02dfa2dba818b9a6c81a9416dfa1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 19:33:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Jun 2026 19:33:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Jun 2026 19:33:41 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:33:41 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Jun 2026 19:33:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:33:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:33:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:33:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ca5dabf7783a6f9f9ce035e047cef313b5969395dd331a6ae02b4888644baf`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f722e30210b3ae00ddc7f9a8e1903197f494d3197297bc2fbf0201008bc826`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 2.7 MB (2663404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fa91218e8453a0f48f968d4e79ec2915ff4e94f9ddd205c806928bcf6401fd`  
		Last Modified: Mon, 08 Jun 2026 19:33:58 GMT  
		Size: 74.5 MB (74541112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca7bb573a3266c7638c7802e066265f0c51f4d1c3b1a8273fc32812d65618ab`  
		Last Modified: Mon, 08 Jun 2026 19:33:55 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:95293b4a78213f540b3e48a94125ce0c51a8f02593c5b9344631a30200610346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a654bf0957227d01a365840e084285d2e1ff416172a723b453027d8bd6cc77b6`

```dockerfile
```

-	Layers:
	-	`sha256:8ad6e19bd77984338905bc7bb0cff26357a4f37f952d6edf88e00b900cc3c4e0`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 1.2 MB (1152750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfff3047d82a9d84c31708e992a7106776945fa93bda13ba3af793b751c0a4f2`  
		Last Modified: Mon, 08 Jun 2026 19:33:55 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:1e53c1f90a46c600e330afed78500dd220586f748e2205f3ffb01bf43fd2c1e3
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
$ docker pull telegraf@sha256:a2f21a5250a4fa7b7136d06b590b6bc1e0231c10508ba2592ecad73963bd5675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175311083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30be059cbbd5776d386a3d02d16643e7451afa3338a6469024d95717094f59e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 19:33:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 19:33:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Jun 2026 19:33:37 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:33:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Jun 2026 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44794ec225e2343d6440e24c585b9198e2780161b5d3f58ba9914efe1995cebd`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 18.9 MB (18944437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f0e48d45af9b728f6d794be505e7620d046e9e2bcbfc03d078f18c19ceacf5`  
		Last Modified: Mon, 08 Jun 2026 19:33:55 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38d408fc19efcf028dd8b9fb79ffc179ea241e1f22b7e7cd2cf3fc7e23846e1`  
		Last Modified: Mon, 08 Jun 2026 19:33:58 GMT  
		Size: 83.8 MB (83822147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc5b42ad8145157934895922fa932fd31f77292ab76762eeb61b7934f5b8270`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:9ee8321238f645b060ebffd167c7bb6dc56082ab62725fc81624f34c683b4df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6687648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4abcb48029b698cbfb6e90a62798f19b5ccaedb581e16e37402e59d171e332`

```dockerfile
```

-	Layers:
	-	`sha256:b7012dd76610a67176c51c48a9186507bf1911a71bb61e5fa22758f940702a79`  
		Last Modified: Mon, 08 Jun 2026 19:33:56 GMT  
		Size: 6.7 MB (6672919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3d8ac59589930741af649402118e1003d6f63e5e8c41cffcf6e89db3e52843`  
		Last Modified: Mon, 08 Jun 2026 19:33:55 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:f16c74c0591b0fe89d146e33021f6a9800e26c2804d979ce49b6d443d0a393f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161566000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c8c3d3444759ad17b9c36c53a706bd2fe316a240ce0f89b2989abccfce80b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 19:31:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 19:31:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Jun 2026 19:32:02 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:32:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Jun 2026 19:32:02 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:32:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:32:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:32:02 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61246c0a5a0fe9fe8cdc1bfde0fdfa49ffafcc94cba31f4aecc0c34bc346064`  
		Last Modified: Wed, 20 May 2026 00:02:11 GMT  
		Size: 22.0 MB (21950133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358c384454c473ff91bcfedb00c1b7ee0442a1f810177b0fea490d34a7872769`  
		Last Modified: Mon, 08 Jun 2026 19:32:20 GMT  
		Size: 17.7 MB (17699712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cb18e97822996823dfd571e1e8a5421960e51d81f073e0c2aa7a0e5825c594`  
		Last Modified: Mon, 08 Jun 2026 19:32:19 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf70df52e08f905db8ad883efdf366eb8d355c181e0e5b2bdfa7b2b7fb885db`  
		Last Modified: Mon, 08 Jun 2026 19:32:21 GMT  
		Size: 77.7 MB (77701323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174cb3db59d9cf34ef1ef55526c70e41a730b3a0554245988b93e7ece5f3004f`  
		Last Modified: Mon, 08 Jun 2026 19:32:19 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:4de53eee522624492737ffb143bb59523110879a0a12cf8c2d210a9ae7964334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2951e7ff9e8f48a6ac85af50eca163949c0f2295bf735e3c350381def1238fd`

```dockerfile
```

-	Layers:
	-	`sha256:5cb4f755f4391fbd3f078e86aa02b31b873f24e82d483bf9223c7402277204fc`  
		Last Modified: Mon, 08 Jun 2026 19:32:19 GMT  
		Size: 6.7 MB (6667524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee08ebbdeb9ca500e807ce802289fc5f4aefeaa4918eadd0a6109ed4a4489d6`  
		Last Modified: Mon, 08 Jun 2026 19:32:19 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2889b1662233d9a474d3455c2de06713af5d502df3ce7c01c402d41cd3b6d937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165632766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71ad10c6f4caa1b61561669a3b82ecb28b5e29b7549902416b4b962ac38d47c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 19:33:38 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 19:33:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 08 Jun 2026 19:33:42 GMT
ENV TELEGRAF_VERSION=1.39.0
# Mon, 08 Jun 2026 19:33:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 08 Jun 2026 19:33:42 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Jun 2026 19:33:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Jun 2026 19:33:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jun 2026 19:33:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17ccd2326ca1cb1f4eed19ded8daa83973465368571f697b4ca8130c9f15c47`  
		Last Modified: Mon, 08 Jun 2026 19:34:01 GMT  
		Size: 18.9 MB (18885895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70342072f85a4fbd0c9c241c273928f9ad6ccce80246650009a546ecb22be8c0`  
		Last Modified: Mon, 08 Jun 2026 19:34:00 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675653bc41056bc54dff03716cdf7c3e37cd3c05f7831862511d875a7f1ad709`  
		Last Modified: Mon, 08 Jun 2026 19:34:02 GMT  
		Size: 74.7 MB (74748367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3327b896e9c815edb5df52b7761ede79230b0e8b3e041624f7847670842c8e08`  
		Last Modified: Mon, 08 Jun 2026 19:34:00 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:ad4eddb6cc3c5706747067e1b3bc53f132379432c0fc0ce2a018adae517ed912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6688458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a96932ecaa7dbeaa9ed2b403bdbec04d0edb5def1291a72d6a3754c9b19c71`

```dockerfile
```

-	Layers:
	-	`sha256:47e4180b8d72a123f8a0950239085557791d37d429960f8022f54ba5ae51c573`  
		Last Modified: Mon, 08 Jun 2026 19:34:00 GMT  
		Size: 6.7 MB (6673607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2c682bef12f5a696c03515cf70cf4658f6e91675ebbd7e7446f561287f6c0be`  
		Last Modified: Mon, 08 Jun 2026 19:34:00 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
