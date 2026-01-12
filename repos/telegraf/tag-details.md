<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.35`](#telegraf135)
-	[`telegraf:1.35-alpine`](#telegraf135-alpine)
-	[`telegraf:1.35.4`](#telegraf1354)
-	[`telegraf:1.35.4-alpine`](#telegraf1354-alpine)
-	[`telegraf:1.36`](#telegraf136)
-	[`telegraf:1.36-alpine`](#telegraf136-alpine)
-	[`telegraf:1.36.4`](#telegraf1364)
-	[`telegraf:1.36.4-alpine`](#telegraf1364-alpine)
-	[`telegraf:1.37`](#telegraf137)
-	[`telegraf:1.37-alpine`](#telegraf137-alpine)
-	[`telegraf:1.37.1`](#telegraf1371)
-	[`telegraf:1.37.1-alpine`](#telegraf1371-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.35`

```console
$ docker pull telegraf@sha256:ee4f29c75215a98e3b6ba9fff1d51a475cd6775b0bcf11194020f5809e430288
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35` - linux; amd64

```console
$ docker pull telegraf@sha256:330ec723dc904cfd41f2830e2e59ee80603efb34ee46661d30b4e317531e40ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171027835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7594ba39ce59c690d83c671f0f84f355f1f15f462fe959693fdb3d4eb0cbc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:43:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:43:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 01:43:45 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 30 Dec 2025 01:43:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 30 Dec 2025 01:43:45 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 30 Dec 2025 01:43:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:43:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:43:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6d146d6dfb878968d9236875dfa584095726b0e0d0c25c1fd4d7e69657f909`  
		Last Modified: Tue, 30 Dec 2025 01:44:14 GMT  
		Size: 18.9 MB (18942949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8792bd0f49708d03a7e69e7b9eb812ad4625478e3a1fe16b68d781b9097c29c7`  
		Last Modified: Tue, 30 Dec 2025 01:44:12 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515b498feae195f0da090a742619cbbc477915b037b1e82122ee9478a1352110`  
		Last Modified: Tue, 30 Dec 2025 01:44:22 GMT  
		Size: 79.6 MB (79570672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0b07d578c29a535d0ea4e489ad31333ddfd1b05dbdf71fbec59d97bc861f9e`  
		Last Modified: Tue, 30 Dec 2025 01:44:12 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:70c9f74a05e97265696aa126490f07828319febd3ceae54060782c9067f62cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef402be4239ad8dce0bba9fe25cc6ef36c7dca7f9ea43202c9999a7f3ae5edd`

```dockerfile
```

-	Layers:
	-	`sha256:3e982cd1802d20b35c9c0514521f29cd3069532bfd8ab58f44cfb10c82ad0d0b`  
		Last Modified: Tue, 30 Dec 2025 04:12:42 GMT  
		Size: 6.6 MB (6644946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70413b186aefa88d7180c867626ddd5cd635d7b986d9ba993b401d4480842b51`  
		Last Modified: Tue, 30 Dec 2025 04:12:42 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:b9d4798da1b0349011eb2434f48d540eabeb30419f317263a9fcfa2921845b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157148201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4170abc57ecfe4eac6a99248dac7d1f48d90955207dd637a38e1783224cd014d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:22:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:22:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 02:22:59 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 30 Dec 2025 02:22:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 30 Dec 2025 02:22:59 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 30 Dec 2025 02:22:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 02:22:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 02:22:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e89c6396ded32c2f8dc71a0c5aae48558ec631543500fcbbe7dbc428401a7361`  
		Last Modified: Mon, 29 Dec 2025 22:25:09 GMT  
		Size: 44.2 MB (44196130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbb8db5ae0eab82c780cd4fa20967bd3633799cf8ed89cd7858d72dcce53203`  
		Last Modified: Tue, 30 Dec 2025 00:33:50 GMT  
		Size: 21.9 MB (21934762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ca29a645c8349dc63b77551409bb6a7fe710ae2e35213b4013cca96f63bb4f`  
		Last Modified: Tue, 30 Dec 2025 02:23:26 GMT  
		Size: 17.7 MB (17722500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ac10bf5edb22c4d565a5a89e08daccf39b79eef00786fdc167c55a212c548`  
		Last Modified: Tue, 30 Dec 2025 02:23:25 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed0935f8c1b91be5b96a7fb9116cdf245bbcacb6113d105756095f628e9751d`  
		Last Modified: Tue, 30 Dec 2025 02:23:31 GMT  
		Size: 73.3 MB (73290742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04029ced2e45d702b6f010e2a752f82e8768fe70813f3d2f9757a0fbb8e2f8c8`  
		Last Modified: Tue, 30 Dec 2025 02:23:25 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:952fed1671cd6a7be98c68e8be2ea9ab169eebeac8b4eb191cbcc40af7df3bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6654060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63415c5ea409e69b90ef40e3b7396876700593e3ab8a84f61bc2a5ab6a47d7a2`

```dockerfile
```

-	Layers:
	-	`sha256:603be2965aecf7fe04fdbe77d017b87c594173d248839ac082c974428f4620cc`  
		Last Modified: Tue, 30 Dec 2025 04:12:48 GMT  
		Size: 6.6 MB (6639543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e90165fbfd384604e25ab4bb7f1ae749033886d2b2d546aa799452d03d2eef6`  
		Last Modified: Tue, 30 Dec 2025 04:12:48 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e694b73032b4c464937ff2d58bbaefa189d8e16acfb64778e282113b56886559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162925439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1149427c3cdba15bb4f67e27f39d6477af74d48be19779af5c14201fcb58abde`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:42:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:42:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 01:42:10 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 30 Dec 2025 01:42:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 30 Dec 2025 01:42:10 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 30 Dec 2025 01:42:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:42:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:42:10 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bb71384090d777b4e1ec8ff484d62a1ef19bef6523ad949cb0f8ab1d72de86`  
		Last Modified: Tue, 30 Dec 2025 01:42:37 GMT  
		Size: 18.9 MB (18884462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81bb4a330c7b5101e62769ed393346cdad91ad975128098cf2e0fe2b2b6cb1d`  
		Last Modified: Tue, 30 Dec 2025 01:42:35 GMT  
		Size: 3.4 KB (3444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bcb26a712f814f6c2fa024e4a9e9ba51fb28da3b6170ff46daacc73e9ef20f`  
		Last Modified: Tue, 30 Dec 2025 01:42:39 GMT  
		Size: 72.1 MB (72079380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f05c3f07bd5ea217822f1d58d8afe12d24d56e1cfa86c27ce7ca3596b8cd11`  
		Last Modified: Tue, 30 Dec 2025 01:42:35 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:1b32d11ff731059c3139be21ba1d7a008af8d613df8317b0f8a9653f2a380860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73faa88cf693e69e58b26630ecfc13b0440ec81517370efea284f6de81b19955`

```dockerfile
```

-	Layers:
	-	`sha256:7a0a8934055e5371a924b007d3dfaa444f9d60e5b26e3e6547667b4dc4daccc0`  
		Last Modified: Tue, 30 Dec 2025 04:13:02 GMT  
		Size: 6.6 MB (6645622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dd7100cb6cede425560eb2bc1a2fb0626db00458b0e1fd957797f894c02895a`  
		Last Modified: Tue, 30 Dec 2025 04:13:03 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35-alpine`

```console
$ docker pull telegraf@sha256:07f7dcf2b3827f051657569751cb64d5faff3e5a72a868693ffb9120e8235879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:218877c5f874e303ce9eff463bd641cd6524d5cb4bf594a918719ce7cb049492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85735517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c39d7be492e6591caa8ad4bed3b416b8e1b0012dabf4da111f2a659a79b3111`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccca5a3c76061483f8823e5d77dd23416fdb6c1db125a11118301458c29897c`  
		Last Modified: Mon, 08 Dec 2025 00:08:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2332823178d0061e80a1f95c48765dbaf18df2dd31878bac57f31fc7e9a9feeb`  
		Last Modified: Mon, 08 Dec 2025 00:08:07 GMT  
		Size: 2.6 MB (2563472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251b8f38f4c764d714567e5ca660283254c5c1f76d6a3eb579385593c3db441f`  
		Last Modified: Mon, 08 Dec 2025 01:56:53 GMT  
		Size: 79.4 MB (79368696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2523c7a219f6fba7e1e9fd8f9a81fbc8fb21f84c41aa6b03e5f001f54fa7d4f`  
		Last Modified: Mon, 08 Dec 2025 00:08:07 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d5f21a0772915320f389bebe6d06e7068c9cfb1211b785a9b3f6333c50c294c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc15951201cadcadb797550a067ab3695eb31ecadbb317a8dbb86766c39fb43f`

```dockerfile
```

-	Layers:
	-	`sha256:f609b510765575f46fd07751df9253b9e0bef412ef4d52e9f96a165469460ed0`  
		Last Modified: Fri, 12 Dec 2025 13:09:25 GMT  
		Size: 1.1 MB (1134008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b8d9f56ca4b6828b99375d962b74da6a704fd9f3bb65cb4e937fc29576512b`  
		Last Modified: Fri, 12 Dec 2025 13:09:24 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2dc98b18a3b682b4d47915f648c59570b29ce00624355c476e03ec8b7437e844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78643760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a73c4abccf0bdf3e9ed8b9eb7c3415a9215de1a7580eefdf2b21df5e598d2ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb651d889db2dee7911408fa57f1d7539c6e6d834e35cef0953d16bae75bf92b`  
		Last Modified: Mon, 08 Dec 2025 11:40:45 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d79a0d11e911af062cf834a3903c2474ae8e732b43633aba958f2e6ad1016b9`  
		Last Modified: Mon, 08 Dec 2025 11:40:46 GMT  
		Size: 2.6 MB (2627489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564facf9ae36962cd5148a9e7a58a23d64ee343b817bdf79fbe0febc06402a3c`  
		Last Modified: Mon, 08 Dec 2025 11:40:48 GMT  
		Size: 71.9 MB (71877304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f7ca04417cf2ffd90adfbbaee47bb81f8f7ebd0b7537bfd13f76b41d9bf2c`  
		Last Modified: Mon, 08 Dec 2025 11:40:45 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4753dbe48b97e81e45692abc4a4cc8c2bea6375210f9d3db090253c6327d3b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ef814572f43a3f8c71c902f5ec20cd44a4e27fb3aa10c609a6532bf95e196a`

```dockerfile
```

-	Layers:
	-	`sha256:eb88913d7607490638a82238d8cb692ac25949af926c0aae25a744e853aec341`  
		Last Modified: Mon, 15 Dec 2025 16:08:52 GMT  
		Size: 1.1 MB (1129635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a5c5dcdefea06875f2d3c71b915b1573aa37fde54d0649aa9189ca1bc85d5a`  
		Last Modified: Mon, 15 Dec 2025 16:08:52 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4`

```console
$ docker pull telegraf@sha256:ee4f29c75215a98e3b6ba9fff1d51a475cd6775b0bcf11194020f5809e430288
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4` - linux; amd64

```console
$ docker pull telegraf@sha256:330ec723dc904cfd41f2830e2e59ee80603efb34ee46661d30b4e317531e40ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171027835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7594ba39ce59c690d83c671f0f84f355f1f15f462fe959693fdb3d4eb0cbc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:43:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:43:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 01:43:45 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 30 Dec 2025 01:43:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 30 Dec 2025 01:43:45 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 30 Dec 2025 01:43:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:43:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:43:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6d146d6dfb878968d9236875dfa584095726b0e0d0c25c1fd4d7e69657f909`  
		Last Modified: Tue, 30 Dec 2025 01:44:14 GMT  
		Size: 18.9 MB (18942949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8792bd0f49708d03a7e69e7b9eb812ad4625478e3a1fe16b68d781b9097c29c7`  
		Last Modified: Tue, 30 Dec 2025 01:44:12 GMT  
		Size: 3.5 KB (3450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515b498feae195f0da090a742619cbbc477915b037b1e82122ee9478a1352110`  
		Last Modified: Tue, 30 Dec 2025 01:44:22 GMT  
		Size: 79.6 MB (79570672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0b07d578c29a535d0ea4e489ad31333ddfd1b05dbdf71fbec59d97bc861f9e`  
		Last Modified: Tue, 30 Dec 2025 01:44:12 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:70c9f74a05e97265696aa126490f07828319febd3ceae54060782c9067f62cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef402be4239ad8dce0bba9fe25cc6ef36c7dca7f9ea43202c9999a7f3ae5edd`

```dockerfile
```

-	Layers:
	-	`sha256:3e982cd1802d20b35c9c0514521f29cd3069532bfd8ab58f44cfb10c82ad0d0b`  
		Last Modified: Tue, 30 Dec 2025 04:12:42 GMT  
		Size: 6.6 MB (6644946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70413b186aefa88d7180c867626ddd5cd635d7b986d9ba993b401d4480842b51`  
		Last Modified: Tue, 30 Dec 2025 04:12:42 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:b9d4798da1b0349011eb2434f48d540eabeb30419f317263a9fcfa2921845b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157148201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4170abc57ecfe4eac6a99248dac7d1f48d90955207dd637a38e1783224cd014d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:22:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:22:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 02:22:59 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 30 Dec 2025 02:22:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 30 Dec 2025 02:22:59 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 30 Dec 2025 02:22:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 02:22:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 02:22:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e89c6396ded32c2f8dc71a0c5aae48558ec631543500fcbbe7dbc428401a7361`  
		Last Modified: Mon, 29 Dec 2025 22:25:09 GMT  
		Size: 44.2 MB (44196130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbb8db5ae0eab82c780cd4fa20967bd3633799cf8ed89cd7858d72dcce53203`  
		Last Modified: Tue, 30 Dec 2025 00:33:50 GMT  
		Size: 21.9 MB (21934762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ca29a645c8349dc63b77551409bb6a7fe710ae2e35213b4013cca96f63bb4f`  
		Last Modified: Tue, 30 Dec 2025 02:23:26 GMT  
		Size: 17.7 MB (17722500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ac10bf5edb22c4d565a5a89e08daccf39b79eef00786fdc167c55a212c548`  
		Last Modified: Tue, 30 Dec 2025 02:23:25 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed0935f8c1b91be5b96a7fb9116cdf245bbcacb6113d105756095f628e9751d`  
		Last Modified: Tue, 30 Dec 2025 02:23:31 GMT  
		Size: 73.3 MB (73290742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04029ced2e45d702b6f010e2a752f82e8768fe70813f3d2f9757a0fbb8e2f8c8`  
		Last Modified: Tue, 30 Dec 2025 02:23:25 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:952fed1671cd6a7be98c68e8be2ea9ab169eebeac8b4eb191cbcc40af7df3bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6654060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63415c5ea409e69b90ef40e3b7396876700593e3ab8a84f61bc2a5ab6a47d7a2`

```dockerfile
```

-	Layers:
	-	`sha256:603be2965aecf7fe04fdbe77d017b87c594173d248839ac082c974428f4620cc`  
		Last Modified: Tue, 30 Dec 2025 04:12:48 GMT  
		Size: 6.6 MB (6639543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e90165fbfd384604e25ab4bb7f1ae749033886d2b2d546aa799452d03d2eef6`  
		Last Modified: Tue, 30 Dec 2025 04:12:48 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:e694b73032b4c464937ff2d58bbaefa189d8e16acfb64778e282113b56886559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162925439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1149427c3cdba15bb4f67e27f39d6477af74d48be19779af5c14201fcb58abde`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:42:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:42:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 01:42:10 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 30 Dec 2025 01:42:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 30 Dec 2025 01:42:10 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 30 Dec 2025 01:42:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:42:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:42:10 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bb71384090d777b4e1ec8ff484d62a1ef19bef6523ad949cb0f8ab1d72de86`  
		Last Modified: Tue, 30 Dec 2025 01:42:37 GMT  
		Size: 18.9 MB (18884462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81bb4a330c7b5101e62769ed393346cdad91ad975128098cf2e0fe2b2b6cb1d`  
		Last Modified: Tue, 30 Dec 2025 01:42:35 GMT  
		Size: 3.4 KB (3444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bcb26a712f814f6c2fa024e4a9e9ba51fb28da3b6170ff46daacc73e9ef20f`  
		Last Modified: Tue, 30 Dec 2025 01:42:39 GMT  
		Size: 72.1 MB (72079380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f05c3f07bd5ea217822f1d58d8afe12d24d56e1cfa86c27ce7ca3596b8cd11`  
		Last Modified: Tue, 30 Dec 2025 01:42:35 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:1b32d11ff731059c3139be21ba1d7a008af8d613df8317b0f8a9653f2a380860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73faa88cf693e69e58b26630ecfc13b0440ec81517370efea284f6de81b19955`

```dockerfile
```

-	Layers:
	-	`sha256:7a0a8934055e5371a924b007d3dfaa444f9d60e5b26e3e6547667b4dc4daccc0`  
		Last Modified: Tue, 30 Dec 2025 04:13:02 GMT  
		Size: 6.6 MB (6645622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dd7100cb6cede425560eb2bc1a2fb0626db00458b0e1fd957797f894c02895a`  
		Last Modified: Tue, 30 Dec 2025 04:13:03 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4-alpine`

```console
$ docker pull telegraf@sha256:07f7dcf2b3827f051657569751cb64d5faff3e5a72a868693ffb9120e8235879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:218877c5f874e303ce9eff463bd641cd6524d5cb4bf594a918719ce7cb049492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85735517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c39d7be492e6591caa8ad4bed3b416b8e1b0012dabf4da111f2a659a79b3111`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccca5a3c76061483f8823e5d77dd23416fdb6c1db125a11118301458c29897c`  
		Last Modified: Mon, 08 Dec 2025 00:08:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2332823178d0061e80a1f95c48765dbaf18df2dd31878bac57f31fc7e9a9feeb`  
		Last Modified: Mon, 08 Dec 2025 00:08:07 GMT  
		Size: 2.6 MB (2563472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251b8f38f4c764d714567e5ca660283254c5c1f76d6a3eb579385593c3db441f`  
		Last Modified: Mon, 08 Dec 2025 01:56:53 GMT  
		Size: 79.4 MB (79368696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2523c7a219f6fba7e1e9fd8f9a81fbc8fb21f84c41aa6b03e5f001f54fa7d4f`  
		Last Modified: Mon, 08 Dec 2025 00:08:07 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d5f21a0772915320f389bebe6d06e7068c9cfb1211b785a9b3f6333c50c294c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc15951201cadcadb797550a067ab3695eb31ecadbb317a8dbb86766c39fb43f`

```dockerfile
```

-	Layers:
	-	`sha256:f609b510765575f46fd07751df9253b9e0bef412ef4d52e9f96a165469460ed0`  
		Last Modified: Fri, 12 Dec 2025 13:09:25 GMT  
		Size: 1.1 MB (1134008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b8d9f56ca4b6828b99375d962b74da6a704fd9f3bb65cb4e937fc29576512b`  
		Last Modified: Fri, 12 Dec 2025 13:09:24 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2dc98b18a3b682b4d47915f648c59570b29ce00624355c476e03ec8b7437e844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78643760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a73c4abccf0bdf3e9ed8b9eb7c3415a9215de1a7580eefdf2b21df5e598d2ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb651d889db2dee7911408fa57f1d7539c6e6d834e35cef0953d16bae75bf92b`  
		Last Modified: Mon, 08 Dec 2025 11:40:45 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d79a0d11e911af062cf834a3903c2474ae8e732b43633aba958f2e6ad1016b9`  
		Last Modified: Mon, 08 Dec 2025 11:40:46 GMT  
		Size: 2.6 MB (2627489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564facf9ae36962cd5148a9e7a58a23d64ee343b817bdf79fbe0febc06402a3c`  
		Last Modified: Mon, 08 Dec 2025 11:40:48 GMT  
		Size: 71.9 MB (71877304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f7ca04417cf2ffd90adfbbaee47bb81f8f7ebd0b7537bfd13f76b41d9bf2c`  
		Last Modified: Mon, 08 Dec 2025 11:40:45 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4753dbe48b97e81e45692abc4a4cc8c2bea6375210f9d3db090253c6327d3b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ef814572f43a3f8c71c902f5ec20cd44a4e27fb3aa10c609a6532bf95e196a`

```dockerfile
```

-	Layers:
	-	`sha256:eb88913d7607490638a82238d8cb692ac25949af926c0aae25a744e853aec341`  
		Last Modified: Mon, 15 Dec 2025 16:08:52 GMT  
		Size: 1.1 MB (1129635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a5c5dcdefea06875f2d3c71b915b1573aa37fde54d0649aa9189ca1bc85d5a`  
		Last Modified: Mon, 15 Dec 2025 16:08:52 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36`

```console
$ docker pull telegraf@sha256:e10d84785d9e3b4b0a0a0c6ad6e6db16df9f19c3f03be9b1d6ccf4f12de8aa7d
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
$ docker pull telegraf@sha256:1a9c494b61352614506e86ce35d31f429f55bfd74bd8bbbb977fafa59914ef16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171930714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1121ede43908c4016eb79006e0c2fa2fd3bc578dfa762e7ab635bd4bcb7adb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:43:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:43:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 01:43:35 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 30 Dec 2025 01:43:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 30 Dec 2025 01:43:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 30 Dec 2025 01:43:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:43:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:43:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3300114d25cf68f83d2fef28cdfcad3512cecdfb133b3a405060e491bed99`  
		Last Modified: Tue, 30 Dec 2025 01:44:05 GMT  
		Size: 18.9 MB (18942982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43903dc791c8c126e4270ca821a14e9ed4f22859784643818a6b9e66099abc3a`  
		Last Modified: Tue, 30 Dec 2025 01:44:01 GMT  
		Size: 3.5 KB (3451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c116e5b130b5d084ee3813c72864ad111246cf33163618235d834c13a3645668`  
		Last Modified: Tue, 30 Dec 2025 01:44:07 GMT  
		Size: 80.5 MB (80473519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662bab21c4a118da465ed3d3ed7cf91f0c6db2605df1786386ad427184f5c314`  
		Last Modified: Tue, 30 Dec 2025 01:44:01 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:0e46a2b022d28064f531ba9129aae2c8fff69fbb3a164e065891228f00ee6c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6667673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77aead44aa689f39da0b1dbe80e89bb185bd37281813a04c445b1a6b1a8ec6cf`

```dockerfile
```

-	Layers:
	-	`sha256:895f1c3dcd8c0f0104cf30baa7f3a7c1d58202116eaf5b3dae26a05372a6d944`  
		Last Modified: Tue, 30 Dec 2025 04:12:57 GMT  
		Size: 6.7 MB (6653246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0efe5f2d714f67414ba1e077551a8095aeb6ff7c9c1d65f4449e1051e65e9151`  
		Last Modified: Tue, 30 Dec 2025 04:12:58 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:5480b87b1ffa2ac63de22d749741f1eabba2f0166630e9fcb7f3216e3fbca0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157820999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786b55a92885acde9b31d14948a85fddbb416f97a85dcf320b3329334edcffc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:23:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:23:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 02:23:19 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 30 Dec 2025 02:23:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 30 Dec 2025 02:23:19 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 30 Dec 2025 02:23:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 02:23:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 02:23:19 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e89c6396ded32c2f8dc71a0c5aae48558ec631543500fcbbe7dbc428401a7361`  
		Last Modified: Mon, 29 Dec 2025 22:25:09 GMT  
		Size: 44.2 MB (44196130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbb8db5ae0eab82c780cd4fa20967bd3633799cf8ed89cd7858d72dcce53203`  
		Last Modified: Tue, 30 Dec 2025 00:33:50 GMT  
		Size: 21.9 MB (21934762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc66809c148648de573aeefbd7e850ba85f2b1e7411901eea98b3cb4a6fa4d9`  
		Last Modified: Tue, 30 Dec 2025 02:23:48 GMT  
		Size: 17.7 MB (17722469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2b1f9076398fa1eb7232c1e37ae92c9877a1fec6b646712c5726f98d983b3f`  
		Last Modified: Tue, 30 Dec 2025 02:23:54 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705a34fdf672539ecfbda1601cc7b9886f02e05dd3e1c71d6966b066d1b3b4f0`  
		Last Modified: Tue, 30 Dec 2025 02:23:54 GMT  
		Size: 74.0 MB (73963573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e9fff87d1e908af4ee30c27b26e751a5d33a6f31af6fab9f2ef1020883a843`  
		Last Modified: Tue, 30 Dec 2025 02:23:46 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:a96e1b4e3b0a80d42b41a8366d156bed1cc969272cd30aad6b8a179e7d406e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e4d6d2ef9d6f2989a1b057bee11973859d4b21d5b2051a576b447ef754b24e`

```dockerfile
```

-	Layers:
	-	`sha256:2fb8242668fbcab38f513deb71e656dc7c18fd18c762edc3ff74f033e4367579`  
		Last Modified: Tue, 30 Dec 2025 04:13:04 GMT  
		Size: 6.6 MB (6647843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bee65f316e8911a102eb8f5ff9ac5a100733f3dfa7bf38ab9f56f65f1fb0abc`  
		Last Modified: Tue, 30 Dec 2025 04:13:04 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:7ba2703b7045de2948d2364e635c3c03a0586a8e41d7d88b4705bbcb2b30376d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162646489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8726bff96468679210572eb6dd185dc84f02246375593bf59ffeaa2276e701d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:45:52 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:45:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 01:45:57 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 30 Dec 2025 01:45:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 30 Dec 2025 01:45:57 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 30 Dec 2025 01:45:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:45:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:45:57 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fab094d098305cdecd806482338abc56fb9e3ddaea1d4f66c2a48e1e6fa231`  
		Last Modified: Tue, 30 Dec 2025 01:46:27 GMT  
		Size: 18.9 MB (18884584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133e7b5d4e17eb9aefa5e68bfdfd76bd46d9cee6c358503c0285d139db15c840`  
		Last Modified: Tue, 30 Dec 2025 01:46:25 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc692499fdacff461d0f846f65d33e61df4c3e38f956370e0c25c9943c9aa9b`  
		Last Modified: Tue, 30 Dec 2025 01:46:35 GMT  
		Size: 71.8 MB (71800313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d56b8dddf8b19cc887f27966f64bbbc939d443ed824bf79201c8e8cf7e1b16a`  
		Last Modified: Tue, 30 Dec 2025 01:46:25 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:8189faf61929567679f220c496c0e24d40c4955c59e795e4bf0d8c93429b9cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6668459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa307df5852952cd9029e059838a7e053ae98b447f6c96bc68355d212499c80e`

```dockerfile
```

-	Layers:
	-	`sha256:d4fce7aa4e42d10d913f930fa20d313aa01926368912a596fb77d3017abf1452`  
		Last Modified: Tue, 30 Dec 2025 04:13:10 GMT  
		Size: 6.7 MB (6653922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37a392367425f5ea3ed53541a2b01544fbdb4b6e0d301b0fb08f8fad9e6d0441`  
		Last Modified: Tue, 30 Dec 2025 04:13:15 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36-alpine`

```console
$ docker pull telegraf@sha256:46cabb477e6e31268bad42966facd2d52c22561d3cfc8d4b0c112b5728ba2c19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:48407b552b16c564ccc47bae44b45ab122d4f48a5bd67d75735d24f586e3f124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86642882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280f08a3c4aeff01bdbeb32bbf32ce8225d3a92ce6199bdfdfabb565fdee4f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 18:59:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:00:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:00:08 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:00:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:00:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb344b979ef9e3d6ea2f360ff66a3139d4cfcd9b863983621de8eefe5cd84aa6`  
		Last Modified: Mon, 17 Nov 2025 19:00:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5696b9b7585c20f57f20c3c7c460662abb184e8eab21a8d4cafd61afc3077a9f`  
		Last Modified: Mon, 17 Nov 2025 19:00:32 GMT  
		Size: 2.6 MB (2563494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff853a04372dd9d1360ee371deb684033ada876ca3c1a38e2d67fe3c5f992aba`  
		Last Modified: Mon, 17 Nov 2025 19:12:22 GMT  
		Size: 80.3 MB (80276038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21db64bfe323b246d3e17e70370a071cbe6e04b604f006cafc7c552ae2a84a58`  
		Last Modified: Mon, 17 Nov 2025 19:00:32 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c9db14f5b6e1db85cf120f8325e5c21fb4b6bc3952dec26a4da8e31845827cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d50f7a3066665cbeb8c985217e41c9d2c2f556ea806eb93be6998e153351815`

```dockerfile
```

-	Layers:
	-	`sha256:d104164b2bcc3c30f646afbdfb9f7942e9d74e4e2e583067261c32c2602a9f20`  
		Last Modified: Mon, 17 Nov 2025 19:10:34 GMT  
		Size: 1.1 MB (1142610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4946291a4533c865cd6bb8bff0320c5aa46fefdae9cb144749cee928ced7711d`  
		Last Modified: Mon, 17 Nov 2025 19:10:35 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4d49d49f81612798363550052fd65d73706db1548e68e0f38576322706f00ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78365616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e73a3d881177da588f763fcd0ab17af8d7f22d8dbad194af635b0bae1274cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 19:02:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:02:18 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:02:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:02:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:02:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e686dad26a4c7f703dc366e1e60b14ae44807c190f97f04760640bb32361676`  
		Last Modified: Mon, 17 Nov 2025 19:02:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d3b38a4228f7da2c38dea9114166ad90b746642df4747865aa32a613fe8247`  
		Last Modified: Mon, 17 Nov 2025 19:02:48 GMT  
		Size: 2.6 MB (2627506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bca33979b5e4d10e8626da8ae6b21afab00ccbeef50beaf1bcd0ad868b8ce7`  
		Last Modified: Mon, 17 Nov 2025 19:02:55 GMT  
		Size: 71.6 MB (71599144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bfa9ad7ce4e4f025b9cfab73b412dc8c04760d6c3ace7fa607998ad9813725`  
		Last Modified: Mon, 17 Nov 2025 19:02:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:b73f976d36f57759d14866b99041351f2aeb2a0facca4b270cf46c7645d8b4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1153591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85106f70e2bf1311bea0e40536625bd137213ea7b96647b802c77c659d7b1b43`

```dockerfile
```

-	Layers:
	-	`sha256:0e40d6658c33f56500ab6ae63559dc1c965812fc29e9404fd354af08b46bc679`  
		Last Modified: Mon, 17 Nov 2025 19:10:39 GMT  
		Size: 1.1 MB (1138249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b269496aa7a00647a4b8e38da5384d0924c563e868cab39620498cdc13c489`  
		Last Modified: Mon, 17 Nov 2025 19:10:40 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4`

```console
$ docker pull telegraf@sha256:e10d84785d9e3b4b0a0a0c6ad6e6db16df9f19c3f03be9b1d6ccf4f12de8aa7d
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
$ docker pull telegraf@sha256:1a9c494b61352614506e86ce35d31f429f55bfd74bd8bbbb977fafa59914ef16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171930714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1121ede43908c4016eb79006e0c2fa2fd3bc578dfa762e7ab635bd4bcb7adb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:43:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:43:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 01:43:35 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 30 Dec 2025 01:43:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 30 Dec 2025 01:43:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 30 Dec 2025 01:43:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:43:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:43:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3300114d25cf68f83d2fef28cdfcad3512cecdfb133b3a405060e491bed99`  
		Last Modified: Tue, 30 Dec 2025 01:44:05 GMT  
		Size: 18.9 MB (18942982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43903dc791c8c126e4270ca821a14e9ed4f22859784643818a6b9e66099abc3a`  
		Last Modified: Tue, 30 Dec 2025 01:44:01 GMT  
		Size: 3.5 KB (3451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c116e5b130b5d084ee3813c72864ad111246cf33163618235d834c13a3645668`  
		Last Modified: Tue, 30 Dec 2025 01:44:07 GMT  
		Size: 80.5 MB (80473519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662bab21c4a118da465ed3d3ed7cf91f0c6db2605df1786386ad427184f5c314`  
		Last Modified: Tue, 30 Dec 2025 01:44:01 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:0e46a2b022d28064f531ba9129aae2c8fff69fbb3a164e065891228f00ee6c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6667673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77aead44aa689f39da0b1dbe80e89bb185bd37281813a04c445b1a6b1a8ec6cf`

```dockerfile
```

-	Layers:
	-	`sha256:895f1c3dcd8c0f0104cf30baa7f3a7c1d58202116eaf5b3dae26a05372a6d944`  
		Last Modified: Tue, 30 Dec 2025 04:12:57 GMT  
		Size: 6.7 MB (6653246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0efe5f2d714f67414ba1e077551a8095aeb6ff7c9c1d65f4449e1051e65e9151`  
		Last Modified: Tue, 30 Dec 2025 04:12:58 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:5480b87b1ffa2ac63de22d749741f1eabba2f0166630e9fcb7f3216e3fbca0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157820999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786b55a92885acde9b31d14948a85fddbb416f97a85dcf320b3329334edcffc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:23:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:23:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 02:23:19 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 30 Dec 2025 02:23:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 30 Dec 2025 02:23:19 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 30 Dec 2025 02:23:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 02:23:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 02:23:19 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e89c6396ded32c2f8dc71a0c5aae48558ec631543500fcbbe7dbc428401a7361`  
		Last Modified: Mon, 29 Dec 2025 22:25:09 GMT  
		Size: 44.2 MB (44196130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbb8db5ae0eab82c780cd4fa20967bd3633799cf8ed89cd7858d72dcce53203`  
		Last Modified: Tue, 30 Dec 2025 00:33:50 GMT  
		Size: 21.9 MB (21934762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc66809c148648de573aeefbd7e850ba85f2b1e7411901eea98b3cb4a6fa4d9`  
		Last Modified: Tue, 30 Dec 2025 02:23:48 GMT  
		Size: 17.7 MB (17722469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2b1f9076398fa1eb7232c1e37ae92c9877a1fec6b646712c5726f98d983b3f`  
		Last Modified: Tue, 30 Dec 2025 02:23:54 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705a34fdf672539ecfbda1601cc7b9886f02e05dd3e1c71d6966b066d1b3b4f0`  
		Last Modified: Tue, 30 Dec 2025 02:23:54 GMT  
		Size: 74.0 MB (73963573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e9fff87d1e908af4ee30c27b26e751a5d33a6f31af6fab9f2ef1020883a843`  
		Last Modified: Tue, 30 Dec 2025 02:23:46 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:a96e1b4e3b0a80d42b41a8366d156bed1cc969272cd30aad6b8a179e7d406e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e4d6d2ef9d6f2989a1b057bee11973859d4b21d5b2051a576b447ef754b24e`

```dockerfile
```

-	Layers:
	-	`sha256:2fb8242668fbcab38f513deb71e656dc7c18fd18c762edc3ff74f033e4367579`  
		Last Modified: Tue, 30 Dec 2025 04:13:04 GMT  
		Size: 6.6 MB (6647843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bee65f316e8911a102eb8f5ff9ac5a100733f3dfa7bf38ab9f56f65f1fb0abc`  
		Last Modified: Tue, 30 Dec 2025 04:13:04 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:7ba2703b7045de2948d2364e635c3c03a0586a8e41d7d88b4705bbcb2b30376d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162646489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8726bff96468679210572eb6dd185dc84f02246375593bf59ffeaa2276e701d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:45:52 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:45:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 01:45:57 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 30 Dec 2025 01:45:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 30 Dec 2025 01:45:57 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 30 Dec 2025 01:45:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:45:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:45:57 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fab094d098305cdecd806482338abc56fb9e3ddaea1d4f66c2a48e1e6fa231`  
		Last Modified: Tue, 30 Dec 2025 01:46:27 GMT  
		Size: 18.9 MB (18884584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133e7b5d4e17eb9aefa5e68bfdfd76bd46d9cee6c358503c0285d139db15c840`  
		Last Modified: Tue, 30 Dec 2025 01:46:25 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc692499fdacff461d0f846f65d33e61df4c3e38f956370e0c25c9943c9aa9b`  
		Last Modified: Tue, 30 Dec 2025 01:46:35 GMT  
		Size: 71.8 MB (71800313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d56b8dddf8b19cc887f27966f64bbbc939d443ed824bf79201c8e8cf7e1b16a`  
		Last Modified: Tue, 30 Dec 2025 01:46:25 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:8189faf61929567679f220c496c0e24d40c4955c59e795e4bf0d8c93429b9cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6668459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa307df5852952cd9029e059838a7e053ae98b447f6c96bc68355d212499c80e`

```dockerfile
```

-	Layers:
	-	`sha256:d4fce7aa4e42d10d913f930fa20d313aa01926368912a596fb77d3017abf1452`  
		Last Modified: Tue, 30 Dec 2025 04:13:10 GMT  
		Size: 6.7 MB (6653922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37a392367425f5ea3ed53541a2b01544fbdb4b6e0d301b0fb08f8fad9e6d0441`  
		Last Modified: Tue, 30 Dec 2025 04:13:15 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4-alpine`

```console
$ docker pull telegraf@sha256:46cabb477e6e31268bad42966facd2d52c22561d3cfc8d4b0c112b5728ba2c19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:48407b552b16c564ccc47bae44b45ab122d4f48a5bd67d75735d24f586e3f124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86642882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280f08a3c4aeff01bdbeb32bbf32ce8225d3a92ce6199bdfdfabb565fdee4f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 18:59:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:00:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:00:08 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:00:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:00:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb344b979ef9e3d6ea2f360ff66a3139d4cfcd9b863983621de8eefe5cd84aa6`  
		Last Modified: Mon, 17 Nov 2025 19:00:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5696b9b7585c20f57f20c3c7c460662abb184e8eab21a8d4cafd61afc3077a9f`  
		Last Modified: Mon, 17 Nov 2025 19:00:32 GMT  
		Size: 2.6 MB (2563494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff853a04372dd9d1360ee371deb684033ada876ca3c1a38e2d67fe3c5f992aba`  
		Last Modified: Mon, 17 Nov 2025 19:12:22 GMT  
		Size: 80.3 MB (80276038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21db64bfe323b246d3e17e70370a071cbe6e04b604f006cafc7c552ae2a84a58`  
		Last Modified: Mon, 17 Nov 2025 19:00:32 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c9db14f5b6e1db85cf120f8325e5c21fb4b6bc3952dec26a4da8e31845827cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d50f7a3066665cbeb8c985217e41c9d2c2f556ea806eb93be6998e153351815`

```dockerfile
```

-	Layers:
	-	`sha256:d104164b2bcc3c30f646afbdfb9f7942e9d74e4e2e583067261c32c2602a9f20`  
		Last Modified: Mon, 17 Nov 2025 19:10:34 GMT  
		Size: 1.1 MB (1142610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4946291a4533c865cd6bb8bff0320c5aa46fefdae9cb144749cee928ced7711d`  
		Last Modified: Mon, 17 Nov 2025 19:10:35 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4d49d49f81612798363550052fd65d73706db1548e68e0f38576322706f00ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78365616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e73a3d881177da588f763fcd0ab17af8d7f22d8dbad194af635b0bae1274cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 19:02:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:02:18 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:02:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:02:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:02:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e686dad26a4c7f703dc366e1e60b14ae44807c190f97f04760640bb32361676`  
		Last Modified: Mon, 17 Nov 2025 19:02:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d3b38a4228f7da2c38dea9114166ad90b746642df4747865aa32a613fe8247`  
		Last Modified: Mon, 17 Nov 2025 19:02:48 GMT  
		Size: 2.6 MB (2627506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bca33979b5e4d10e8626da8ae6b21afab00ccbeef50beaf1bcd0ad868b8ce7`  
		Last Modified: Mon, 17 Nov 2025 19:02:55 GMT  
		Size: 71.6 MB (71599144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bfa9ad7ce4e4f025b9cfab73b412dc8c04760d6c3ace7fa607998ad9813725`  
		Last Modified: Mon, 17 Nov 2025 19:02:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:b73f976d36f57759d14866b99041351f2aeb2a0facca4b270cf46c7645d8b4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1153591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85106f70e2bf1311bea0e40536625bd137213ea7b96647b802c77c659d7b1b43`

```dockerfile
```

-	Layers:
	-	`sha256:0e40d6658c33f56500ab6ae63559dc1c965812fc29e9404fd354af08b46bc679`  
		Last Modified: Mon, 17 Nov 2025 19:10:39 GMT  
		Size: 1.1 MB (1138249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b269496aa7a00647a4b8e38da5384d0924c563e868cab39620498cdc13c489`  
		Last Modified: Mon, 17 Nov 2025 19:10:40 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37`

```console
$ docker pull telegraf@sha256:c7318e4e7c5d96c45dcebe115439387892904450a92aa4ffea0881a0eb6bedd0
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
$ docker pull telegraf@sha256:4425911ca253ee7cc9433decd4f45f1253d4fcd3153a2a315c9e269d26b29dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171908969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2e66a9e52b14bdb63282c824de95577d5c1d9e7e2b437dd3f3f3db97e34f48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 22:03:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 22:03:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Jan 2026 22:03:29 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:03:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Jan 2026 22:03:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:03:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:03:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:03:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f4c8995e83e1e99f47bc0e6453bf779ca3b64c224943fc38b442e3cb2383b6`  
		Last Modified: Mon, 12 Jan 2026 22:04:05 GMT  
		Size: 19.0 MB (18974347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed577b3fde577f26add54efbfc4fc204f30acbe8ee1bfd29a45b115260ef72c8`  
		Last Modified: Mon, 12 Jan 2026 22:04:03 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09de6373d3eec39836dcfb3e97ccf6f1f8f4da6cba5ed734f1ddd096d86a2f3`  
		Last Modified: Mon, 12 Jan 2026 22:04:18 GMT  
		Size: 80.4 MB (80418802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4933ab140a827dc2acb4949947951af770408107cccce78e82a029cbb933bdd8`  
		Last Modified: Mon, 12 Jan 2026 22:04:04 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:2bde558ab8811d0510bd5ad58fee7787ab8e5d5d391a72cef1aeb5462003695e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706194781c2aeeff685b10554fa82efe8884750056f884d368c9b4ae6804b53b`

```dockerfile
```

-	Layers:
	-	`sha256:10a8aa12d3b0353680e5c114c631f90d91b11d3203db606e8ae2cae210d384d7`  
		Last Modified: Mon, 12 Jan 2026 22:10:29 GMT  
		Size: 6.7 MB (6667264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce07c6c24a7b7b3495075ac6f68d68f2acd4a39cae38c49a74486319e3296aa0`  
		Last Modified: Mon, 12 Jan 2026 22:10:31 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:db620ce1550fd426cddc168547452bc5116b161f578788c13dbd58d049162e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158136402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9b493e401e643da6ba3d754cde3e16c2faed49456ea7e5fb423d89a84ff965`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 22:02:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 22:02:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Jan 2026 22:02:12 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:02:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Jan 2026 22:02:12 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:02:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:02:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:02:12 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e89c6396ded32c2f8dc71a0c5aae48558ec631543500fcbbe7dbc428401a7361`  
		Last Modified: Mon, 29 Dec 2025 22:25:09 GMT  
		Size: 44.2 MB (44196130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbb8db5ae0eab82c780cd4fa20967bd3633799cf8ed89cd7858d72dcce53203`  
		Last Modified: Tue, 30 Dec 2025 00:33:50 GMT  
		Size: 21.9 MB (21934762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a2bb2bf40b0e1b4f74bc6c6ea7a21a5c7fcb99288a7e6583b6e154c473eee7`  
		Last Modified: Mon, 12 Jan 2026 22:02:46 GMT  
		Size: 17.7 MB (17716560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c52a8c81a62968ef852eac838260a45ad53432cb520a5cb1040781f8522e3b1`  
		Last Modified: Mon, 12 Jan 2026 22:02:44 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a757506830c1ecc79a15882d458af2c7a6d081023581248afad2c4aa5520d7`  
		Last Modified: Mon, 12 Jan 2026 22:02:54 GMT  
		Size: 74.3 MB (74283272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658d9b4d2d84d37b19e67abf950b3a8c63b0c4facff8ecc7c9c0af2fe331c6bc`  
		Last Modified: Mon, 12 Jan 2026 22:02:44 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:ceb60fc0226cec73ba3ef7c0c69f8bf215d34248cb1002a2a7f1a3d8c74a0079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a78f4455dc90d3d2e2207022f8952c3c87dfd7fdc692635c5dad73d9aae7f4`

```dockerfile
```

-	Layers:
	-	`sha256:1104854031d6a6c4e6eef8b0dc55c705b265d1fb9e5cccf38e637510a1146d56`  
		Last Modified: Mon, 12 Jan 2026 22:10:49 GMT  
		Size: 6.7 MB (6661869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3daf0af6e121d599227f253bbc2794a796aa28c3ed9e65da48e2024952de19a`  
		Last Modified: Mon, 12 Jan 2026 22:10:50 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c2c103d6c16d2004992903326db5982d62be8eebd37c6968cb1814b357e795d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162724371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb381561a0d3741b950454fabb42562efd4200f51e244654d5a131b6061b89fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 22:03:42 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 22:03:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Jan 2026 22:03:48 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:03:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Jan 2026 22:03:48 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:03:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:03:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:03:48 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4252bf63e8bf805cfee4290fc1d3bdc401f4515a8c020f037b24cdb979852b5`  
		Last Modified: Mon, 12 Jan 2026 22:04:27 GMT  
		Size: 18.9 MB (18924390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef93afc870463a02d101ab9654f6eb9f96c107e96934aa172dbdaedea6d4ddee`  
		Last Modified: Mon, 12 Jan 2026 22:04:25 GMT  
		Size: 5.1 KB (5058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5773e41357d39b560948402565c0769acba6fd8af0f710abfaac3022e634e48`  
		Last Modified: Mon, 12 Jan 2026 22:04:34 GMT  
		Size: 71.8 MB (71836772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a810e5f6e2cda97e1f18cd7a6f7b389113b40e17dc81f8b34ea641ba3e43a96`  
		Last Modified: Mon, 12 Jan 2026 22:04:25 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:a3d7a580de3b6c7725de5599ce5b6c510fbad427ab22574835faaeed124d5591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f06d7a33125b6ee7a66e6397e9b03b44f4db9f2a8a7846abd8bd9aea1d5660`

```dockerfile
```

-	Layers:
	-	`sha256:ec2f999e1d3274eae2fdf8fbc1c54156da8845ac7e9c6b4671af382c8dafe783`  
		Last Modified: Mon, 12 Jan 2026 22:10:56 GMT  
		Size: 6.7 MB (6667952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74bce7308f4835d23ab5ba3cc11449864217adbbcb0f1dfbe95ee1245aff9c00`  
		Last Modified: Mon, 12 Jan 2026 22:10:57 GMT  
		Size: 14.8 KB (14850 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37-alpine`

```console
$ docker pull telegraf@sha256:da425d612a6562dd10e0c451e6c4eb8afd167cdc57f3c6e8e9671eef96970b40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b34930ce34197c6817195c87a9ceb42ac71e7aa324dfaa3020c38242a3c91947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86579178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c4937d4147e1e76854674e70f7a078d846f280232f989a537f1bf798e0d439`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 12 Jan 2026 22:03:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Jan 2026 22:03:58 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 12 Jan 2026 22:04:06 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:04:06 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Jan 2026 22:04:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:04:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:04:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:04:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0006f07fa7aa837946a8af5d498120b48885b0a5a02c9929d7a1551c00c35f79`  
		Last Modified: Mon, 12 Jan 2026 22:04:29 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34baf35d0c044c243bbbaefc8624d74fafaaf5352d5fcac982da66fd6eb5a22d`  
		Last Modified: Mon, 12 Jan 2026 22:04:31 GMT  
		Size: 2.6 MB (2563615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09297e8e447d6e5d15537473611c206598fe67e40163f9df8f6a70625ed054a`  
		Last Modified: Mon, 12 Jan 2026 22:04:43 GMT  
		Size: 80.2 MB (80212211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f557f91ca62469816ba86af69d33a347b7a268757860c5c75ee5a2b37c91aa`  
		Last Modified: Mon, 12 Jan 2026 22:04:29 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:7192889210b0d2a19dcf67c8c58ec2760bb49329e21c2e59cba027ec86a4fd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b96b7453f34b1b9c00194ce3f030a6c778a2e35b0d98a50c2ab271cd872f17`

```dockerfile
```

-	Layers:
	-	`sha256:d9e3f695b0d400877243266abe78ae2bd0a13b3f9fe68b331458a2e88db9b2be`  
		Last Modified: Mon, 12 Jan 2026 22:10:37 GMT  
		Size: 1.2 MB (1153471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0988d676a18b75ab875f5be5d1fdf99d16a05b1ba44dd7b33021b01eca13e07b`  
		Last Modified: Mon, 12 Jan 2026 22:10:38 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0763e04a854f82c70f01060f43ef8410836173a3b8d1c24de2ad347c882cc89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78396849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc5cfe6009708d43fead662b5b2158f07259261ec4bb2f04b8578dd0d55ea70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 12 Jan 2026 22:04:15 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Jan 2026 22:04:17 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 12 Jan 2026 22:04:24 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:04:24 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Jan 2026 22:04:24 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:04:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:04:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:04:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1301b68b009329cd05b051fd8942099cfca0f90d771fa70b9d1dc51b4a8c4a`  
		Last Modified: Mon, 12 Jan 2026 22:04:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669d920cdb42e86e3e59b78a7f8edc2a98f16b82d01d5e8ad2efc4da60b6bb36`  
		Last Modified: Mon, 12 Jan 2026 22:04:47 GMT  
		Size: 2.6 MB (2627638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462024f532776566fd3272f6a12fef0a525de3afa955d8a7052c5d10e0dce9ca`  
		Last Modified: Mon, 12 Jan 2026 22:04:53 GMT  
		Size: 71.6 MB (71630243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d679e78c84ba62ae726d2097b1e5bbed0c24b995736a357f7606235e33fb2fc6`  
		Last Modified: Mon, 12 Jan 2026 22:04:47 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:846491217fca7d5ec7c094397cfbcdbabc951b578490d0d5518d83f37e2eb565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e60147038d2ac3bedd7de0f47888bc221f044e9564bf3a8b19440b62a384a54`

```dockerfile
```

-	Layers:
	-	`sha256:62bc1c5598388899ccad1663492c6cca79651b20470c658d4f5cc43650d0a291`  
		Last Modified: Mon, 12 Jan 2026 22:10:43 GMT  
		Size: 1.1 MB (1149110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3919d3cbeb355252044e48eb284dbdd17931390f6452ecf5e3079f9e19006c1`  
		Last Modified: Mon, 12 Jan 2026 22:10:43 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.1`

```console
$ docker pull telegraf@sha256:c7318e4e7c5d96c45dcebe115439387892904450a92aa4ffea0881a0eb6bedd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.1` - linux; amd64

```console
$ docker pull telegraf@sha256:4425911ca253ee7cc9433decd4f45f1253d4fcd3153a2a315c9e269d26b29dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171908969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2e66a9e52b14bdb63282c824de95577d5c1d9e7e2b437dd3f3f3db97e34f48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 22:03:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 22:03:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Jan 2026 22:03:29 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:03:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Jan 2026 22:03:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:03:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:03:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:03:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f4c8995e83e1e99f47bc0e6453bf779ca3b64c224943fc38b442e3cb2383b6`  
		Last Modified: Mon, 12 Jan 2026 22:04:05 GMT  
		Size: 19.0 MB (18974347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed577b3fde577f26add54efbfc4fc204f30acbe8ee1bfd29a45b115260ef72c8`  
		Last Modified: Mon, 12 Jan 2026 22:04:03 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09de6373d3eec39836dcfb3e97ccf6f1f8f4da6cba5ed734f1ddd096d86a2f3`  
		Last Modified: Mon, 12 Jan 2026 22:04:18 GMT  
		Size: 80.4 MB (80418802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4933ab140a827dc2acb4949947951af770408107cccce78e82a029cbb933bdd8`  
		Last Modified: Mon, 12 Jan 2026 22:04:04 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:2bde558ab8811d0510bd5ad58fee7787ab8e5d5d391a72cef1aeb5462003695e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706194781c2aeeff685b10554fa82efe8884750056f884d368c9b4ae6804b53b`

```dockerfile
```

-	Layers:
	-	`sha256:10a8aa12d3b0353680e5c114c631f90d91b11d3203db606e8ae2cae210d384d7`  
		Last Modified: Mon, 12 Jan 2026 22:10:29 GMT  
		Size: 6.7 MB (6667264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce07c6c24a7b7b3495075ac6f68d68f2acd4a39cae38c49a74486319e3296aa0`  
		Last Modified: Mon, 12 Jan 2026 22:10:31 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.1` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:db620ce1550fd426cddc168547452bc5116b161f578788c13dbd58d049162e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158136402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9b493e401e643da6ba3d754cde3e16c2faed49456ea7e5fb423d89a84ff965`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 22:02:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 22:02:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Jan 2026 22:02:12 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:02:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Jan 2026 22:02:12 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:02:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:02:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:02:12 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e89c6396ded32c2f8dc71a0c5aae48558ec631543500fcbbe7dbc428401a7361`  
		Last Modified: Mon, 29 Dec 2025 22:25:09 GMT  
		Size: 44.2 MB (44196130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbb8db5ae0eab82c780cd4fa20967bd3633799cf8ed89cd7858d72dcce53203`  
		Last Modified: Tue, 30 Dec 2025 00:33:50 GMT  
		Size: 21.9 MB (21934762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a2bb2bf40b0e1b4f74bc6c6ea7a21a5c7fcb99288a7e6583b6e154c473eee7`  
		Last Modified: Mon, 12 Jan 2026 22:02:46 GMT  
		Size: 17.7 MB (17716560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c52a8c81a62968ef852eac838260a45ad53432cb520a5cb1040781f8522e3b1`  
		Last Modified: Mon, 12 Jan 2026 22:02:44 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a757506830c1ecc79a15882d458af2c7a6d081023581248afad2c4aa5520d7`  
		Last Modified: Mon, 12 Jan 2026 22:02:54 GMT  
		Size: 74.3 MB (74283272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658d9b4d2d84d37b19e67abf950b3a8c63b0c4facff8ecc7c9c0af2fe331c6bc`  
		Last Modified: Mon, 12 Jan 2026 22:02:44 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:ceb60fc0226cec73ba3ef7c0c69f8bf215d34248cb1002a2a7f1a3d8c74a0079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a78f4455dc90d3d2e2207022f8952c3c87dfd7fdc692635c5dad73d9aae7f4`

```dockerfile
```

-	Layers:
	-	`sha256:1104854031d6a6c4e6eef8b0dc55c705b265d1fb9e5cccf38e637510a1146d56`  
		Last Modified: Mon, 12 Jan 2026 22:10:49 GMT  
		Size: 6.7 MB (6661869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3daf0af6e121d599227f253bbc2794a796aa28c3ed9e65da48e2024952de19a`  
		Last Modified: Mon, 12 Jan 2026 22:10:50 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.1` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c2c103d6c16d2004992903326db5982d62be8eebd37c6968cb1814b357e795d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162724371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb381561a0d3741b950454fabb42562efd4200f51e244654d5a131b6061b89fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 22:03:42 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 22:03:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Jan 2026 22:03:48 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:03:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Jan 2026 22:03:48 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:03:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:03:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:03:48 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4252bf63e8bf805cfee4290fc1d3bdc401f4515a8c020f037b24cdb979852b5`  
		Last Modified: Mon, 12 Jan 2026 22:04:27 GMT  
		Size: 18.9 MB (18924390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef93afc870463a02d101ab9654f6eb9f96c107e96934aa172dbdaedea6d4ddee`  
		Last Modified: Mon, 12 Jan 2026 22:04:25 GMT  
		Size: 5.1 KB (5058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5773e41357d39b560948402565c0769acba6fd8af0f710abfaac3022e634e48`  
		Last Modified: Mon, 12 Jan 2026 22:04:34 GMT  
		Size: 71.8 MB (71836772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a810e5f6e2cda97e1f18cd7a6f7b389113b40e17dc81f8b34ea641ba3e43a96`  
		Last Modified: Mon, 12 Jan 2026 22:04:25 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.1` - unknown; unknown

```console
$ docker pull telegraf@sha256:a3d7a580de3b6c7725de5599ce5b6c510fbad427ab22574835faaeed124d5591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f06d7a33125b6ee7a66e6397e9b03b44f4db9f2a8a7846abd8bd9aea1d5660`

```dockerfile
```

-	Layers:
	-	`sha256:ec2f999e1d3274eae2fdf8fbc1c54156da8845ac7e9c6b4671af382c8dafe783`  
		Last Modified: Mon, 12 Jan 2026 22:10:56 GMT  
		Size: 6.7 MB (6667952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74bce7308f4835d23ab5ba3cc11449864217adbbcb0f1dfbe95ee1245aff9c00`  
		Last Modified: Mon, 12 Jan 2026 22:10:57 GMT  
		Size: 14.8 KB (14850 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.1-alpine`

```console
$ docker pull telegraf@sha256:da425d612a6562dd10e0c451e6c4eb8afd167cdc57f3c6e8e9671eef96970b40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.1-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b34930ce34197c6817195c87a9ceb42ac71e7aa324dfaa3020c38242a3c91947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86579178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c4937d4147e1e76854674e70f7a078d846f280232f989a537f1bf798e0d439`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 12 Jan 2026 22:03:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Jan 2026 22:03:58 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 12 Jan 2026 22:04:06 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:04:06 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Jan 2026 22:04:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:04:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:04:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:04:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0006f07fa7aa837946a8af5d498120b48885b0a5a02c9929d7a1551c00c35f79`  
		Last Modified: Mon, 12 Jan 2026 22:04:29 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34baf35d0c044c243bbbaefc8624d74fafaaf5352d5fcac982da66fd6eb5a22d`  
		Last Modified: Mon, 12 Jan 2026 22:04:31 GMT  
		Size: 2.6 MB (2563615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09297e8e447d6e5d15537473611c206598fe67e40163f9df8f6a70625ed054a`  
		Last Modified: Mon, 12 Jan 2026 22:04:43 GMT  
		Size: 80.2 MB (80212211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f557f91ca62469816ba86af69d33a347b7a268757860c5c75ee5a2b37c91aa`  
		Last Modified: Mon, 12 Jan 2026 22:04:29 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.1-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:7192889210b0d2a19dcf67c8c58ec2760bb49329e21c2e59cba027ec86a4fd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b96b7453f34b1b9c00194ce3f030a6c778a2e35b0d98a50c2ab271cd872f17`

```dockerfile
```

-	Layers:
	-	`sha256:d9e3f695b0d400877243266abe78ae2bd0a13b3f9fe68b331458a2e88db9b2be`  
		Last Modified: Mon, 12 Jan 2026 22:10:37 GMT  
		Size: 1.2 MB (1153471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0988d676a18b75ab875f5be5d1fdf99d16a05b1ba44dd7b33021b01eca13e07b`  
		Last Modified: Mon, 12 Jan 2026 22:10:38 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.1-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0763e04a854f82c70f01060f43ef8410836173a3b8d1c24de2ad347c882cc89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78396849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc5cfe6009708d43fead662b5b2158f07259261ec4bb2f04b8578dd0d55ea70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 12 Jan 2026 22:04:15 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Jan 2026 22:04:17 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 12 Jan 2026 22:04:24 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:04:24 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Jan 2026 22:04:24 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:04:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:04:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:04:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1301b68b009329cd05b051fd8942099cfca0f90d771fa70b9d1dc51b4a8c4a`  
		Last Modified: Mon, 12 Jan 2026 22:04:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669d920cdb42e86e3e59b78a7f8edc2a98f16b82d01d5e8ad2efc4da60b6bb36`  
		Last Modified: Mon, 12 Jan 2026 22:04:47 GMT  
		Size: 2.6 MB (2627638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462024f532776566fd3272f6a12fef0a525de3afa955d8a7052c5d10e0dce9ca`  
		Last Modified: Mon, 12 Jan 2026 22:04:53 GMT  
		Size: 71.6 MB (71630243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d679e78c84ba62ae726d2097b1e5bbed0c24b995736a357f7606235e33fb2fc6`  
		Last Modified: Mon, 12 Jan 2026 22:04:47 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.1-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:846491217fca7d5ec7c094397cfbcdbabc951b578490d0d5518d83f37e2eb565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e60147038d2ac3bedd7de0f47888bc221f044e9564bf3a8b19440b62a384a54`

```dockerfile
```

-	Layers:
	-	`sha256:62bc1c5598388899ccad1663492c6cca79651b20470c658d4f5cc43650d0a291`  
		Last Modified: Mon, 12 Jan 2026 22:10:43 GMT  
		Size: 1.1 MB (1149110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3919d3cbeb355252044e48eb284dbdd17931390f6452ecf5e3079f9e19006c1`  
		Last Modified: Mon, 12 Jan 2026 22:10:43 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:da425d612a6562dd10e0c451e6c4eb8afd167cdc57f3c6e8e9671eef96970b40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b34930ce34197c6817195c87a9ceb42ac71e7aa324dfaa3020c38242a3c91947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86579178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c4937d4147e1e76854674e70f7a078d846f280232f989a537f1bf798e0d439`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 12 Jan 2026 22:03:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Jan 2026 22:03:58 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 12 Jan 2026 22:04:06 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:04:06 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Jan 2026 22:04:06 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:04:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:04:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:04:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0006f07fa7aa837946a8af5d498120b48885b0a5a02c9929d7a1551c00c35f79`  
		Last Modified: Mon, 12 Jan 2026 22:04:29 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34baf35d0c044c243bbbaefc8624d74fafaaf5352d5fcac982da66fd6eb5a22d`  
		Last Modified: Mon, 12 Jan 2026 22:04:31 GMT  
		Size: 2.6 MB (2563615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09297e8e447d6e5d15537473611c206598fe67e40163f9df8f6a70625ed054a`  
		Last Modified: Mon, 12 Jan 2026 22:04:43 GMT  
		Size: 80.2 MB (80212211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f557f91ca62469816ba86af69d33a347b7a268757860c5c75ee5a2b37c91aa`  
		Last Modified: Mon, 12 Jan 2026 22:04:29 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:7192889210b0d2a19dcf67c8c58ec2760bb49329e21c2e59cba027ec86a4fd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b96b7453f34b1b9c00194ce3f030a6c778a2e35b0d98a50c2ab271cd872f17`

```dockerfile
```

-	Layers:
	-	`sha256:d9e3f695b0d400877243266abe78ae2bd0a13b3f9fe68b331458a2e88db9b2be`  
		Last Modified: Mon, 12 Jan 2026 22:10:37 GMT  
		Size: 1.2 MB (1153471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0988d676a18b75ab875f5be5d1fdf99d16a05b1ba44dd7b33021b01eca13e07b`  
		Last Modified: Mon, 12 Jan 2026 22:10:38 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0763e04a854f82c70f01060f43ef8410836173a3b8d1c24de2ad347c882cc89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78396849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc5cfe6009708d43fead662b5b2158f07259261ec4bb2f04b8578dd0d55ea70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 12 Jan 2026 22:04:15 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Jan 2026 22:04:17 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 12 Jan 2026 22:04:24 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:04:24 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Jan 2026 22:04:24 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:04:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:04:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:04:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1301b68b009329cd05b051fd8942099cfca0f90d771fa70b9d1dc51b4a8c4a`  
		Last Modified: Mon, 12 Jan 2026 22:04:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669d920cdb42e86e3e59b78a7f8edc2a98f16b82d01d5e8ad2efc4da60b6bb36`  
		Last Modified: Mon, 12 Jan 2026 22:04:47 GMT  
		Size: 2.6 MB (2627638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462024f532776566fd3272f6a12fef0a525de3afa955d8a7052c5d10e0dce9ca`  
		Last Modified: Mon, 12 Jan 2026 22:04:53 GMT  
		Size: 71.6 MB (71630243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d679e78c84ba62ae726d2097b1e5bbed0c24b995736a357f7606235e33fb2fc6`  
		Last Modified: Mon, 12 Jan 2026 22:04:47 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:846491217fca7d5ec7c094397cfbcdbabc951b578490d0d5518d83f37e2eb565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e60147038d2ac3bedd7de0f47888bc221f044e9564bf3a8b19440b62a384a54`

```dockerfile
```

-	Layers:
	-	`sha256:62bc1c5598388899ccad1663492c6cca79651b20470c658d4f5cc43650d0a291`  
		Last Modified: Mon, 12 Jan 2026 22:10:43 GMT  
		Size: 1.1 MB (1149110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3919d3cbeb355252044e48eb284dbdd17931390f6452ecf5e3079f9e19006c1`  
		Last Modified: Mon, 12 Jan 2026 22:10:43 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:c7318e4e7c5d96c45dcebe115439387892904450a92aa4ffea0881a0eb6bedd0
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
$ docker pull telegraf@sha256:4425911ca253ee7cc9433decd4f45f1253d4fcd3153a2a315c9e269d26b29dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171908969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2e66a9e52b14bdb63282c824de95577d5c1d9e7e2b437dd3f3f3db97e34f48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 22:03:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 22:03:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Jan 2026 22:03:29 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:03:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Jan 2026 22:03:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:03:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:03:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:03:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f4c8995e83e1e99f47bc0e6453bf779ca3b64c224943fc38b442e3cb2383b6`  
		Last Modified: Mon, 12 Jan 2026 22:04:05 GMT  
		Size: 19.0 MB (18974347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed577b3fde577f26add54efbfc4fc204f30acbe8ee1bfd29a45b115260ef72c8`  
		Last Modified: Mon, 12 Jan 2026 22:04:03 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09de6373d3eec39836dcfb3e97ccf6f1f8f4da6cba5ed734f1ddd096d86a2f3`  
		Last Modified: Mon, 12 Jan 2026 22:04:18 GMT  
		Size: 80.4 MB (80418802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4933ab140a827dc2acb4949947951af770408107cccce78e82a029cbb933bdd8`  
		Last Modified: Mon, 12 Jan 2026 22:04:04 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:2bde558ab8811d0510bd5ad58fee7787ab8e5d5d391a72cef1aeb5462003695e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706194781c2aeeff685b10554fa82efe8884750056f884d368c9b4ae6804b53b`

```dockerfile
```

-	Layers:
	-	`sha256:10a8aa12d3b0353680e5c114c631f90d91b11d3203db606e8ae2cae210d384d7`  
		Last Modified: Mon, 12 Jan 2026 22:10:29 GMT  
		Size: 6.7 MB (6667264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce07c6c24a7b7b3495075ac6f68d68f2acd4a39cae38c49a74486319e3296aa0`  
		Last Modified: Mon, 12 Jan 2026 22:10:31 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:db620ce1550fd426cddc168547452bc5116b161f578788c13dbd58d049162e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158136402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9b493e401e643da6ba3d754cde3e16c2faed49456ea7e5fb423d89a84ff965`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 22:02:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 22:02:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Jan 2026 22:02:12 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:02:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Jan 2026 22:02:12 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:02:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:02:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:02:12 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e89c6396ded32c2f8dc71a0c5aae48558ec631543500fcbbe7dbc428401a7361`  
		Last Modified: Mon, 29 Dec 2025 22:25:09 GMT  
		Size: 44.2 MB (44196130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbb8db5ae0eab82c780cd4fa20967bd3633799cf8ed89cd7858d72dcce53203`  
		Last Modified: Tue, 30 Dec 2025 00:33:50 GMT  
		Size: 21.9 MB (21934762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a2bb2bf40b0e1b4f74bc6c6ea7a21a5c7fcb99288a7e6583b6e154c473eee7`  
		Last Modified: Mon, 12 Jan 2026 22:02:46 GMT  
		Size: 17.7 MB (17716560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c52a8c81a62968ef852eac838260a45ad53432cb520a5cb1040781f8522e3b1`  
		Last Modified: Mon, 12 Jan 2026 22:02:44 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a757506830c1ecc79a15882d458af2c7a6d081023581248afad2c4aa5520d7`  
		Last Modified: Mon, 12 Jan 2026 22:02:54 GMT  
		Size: 74.3 MB (74283272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658d9b4d2d84d37b19e67abf950b3a8c63b0c4facff8ecc7c9c0af2fe331c6bc`  
		Last Modified: Mon, 12 Jan 2026 22:02:44 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:ceb60fc0226cec73ba3ef7c0c69f8bf215d34248cb1002a2a7f1a3d8c74a0079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a78f4455dc90d3d2e2207022f8952c3c87dfd7fdc692635c5dad73d9aae7f4`

```dockerfile
```

-	Layers:
	-	`sha256:1104854031d6a6c4e6eef8b0dc55c705b265d1fb9e5cccf38e637510a1146d56`  
		Last Modified: Mon, 12 Jan 2026 22:10:49 GMT  
		Size: 6.7 MB (6661869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3daf0af6e121d599227f253bbc2794a796aa28c3ed9e65da48e2024952de19a`  
		Last Modified: Mon, 12 Jan 2026 22:10:50 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c2c103d6c16d2004992903326db5982d62be8eebd37c6968cb1814b357e795d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162724371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb381561a0d3741b950454fabb42562efd4200f51e244654d5a131b6061b89fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 22:03:42 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 22:03:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Jan 2026 22:03:48 GMT
ENV TELEGRAF_VERSION=1.37.1
# Mon, 12 Jan 2026 22:03:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Jan 2026 22:03:48 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Jan 2026 22:03:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Jan 2026 22:03:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Jan 2026 22:03:48 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4252bf63e8bf805cfee4290fc1d3bdc401f4515a8c020f037b24cdb979852b5`  
		Last Modified: Mon, 12 Jan 2026 22:04:27 GMT  
		Size: 18.9 MB (18924390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef93afc870463a02d101ab9654f6eb9f96c107e96934aa172dbdaedea6d4ddee`  
		Last Modified: Mon, 12 Jan 2026 22:04:25 GMT  
		Size: 5.1 KB (5058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5773e41357d39b560948402565c0769acba6fd8af0f710abfaac3022e634e48`  
		Last Modified: Mon, 12 Jan 2026 22:04:34 GMT  
		Size: 71.8 MB (71836772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a810e5f6e2cda97e1f18cd7a6f7b389113b40e17dc81f8b34ea641ba3e43a96`  
		Last Modified: Mon, 12 Jan 2026 22:04:25 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:a3d7a580de3b6c7725de5599ce5b6c510fbad427ab22574835faaeed124d5591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f06d7a33125b6ee7a66e6397e9b03b44f4db9f2a8a7846abd8bd9aea1d5660`

```dockerfile
```

-	Layers:
	-	`sha256:ec2f999e1d3274eae2fdf8fbc1c54156da8845ac7e9c6b4671af382c8dafe783`  
		Last Modified: Mon, 12 Jan 2026 22:10:56 GMT  
		Size: 6.7 MB (6667952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74bce7308f4835d23ab5ba3cc11449864217adbbcb0f1dfbe95ee1245aff9c00`  
		Last Modified: Mon, 12 Jan 2026 22:10:57 GMT  
		Size: 14.8 KB (14850 bytes)  
		MIME: application/vnd.in-toto+json
