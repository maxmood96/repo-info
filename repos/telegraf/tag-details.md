<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.26`](#telegraf126)
-	[`telegraf:1.26-alpine`](#telegraf126-alpine)
-	[`telegraf:1.26.3`](#telegraf1263)
-	[`telegraf:1.26.3-alpine`](#telegraf1263-alpine)
-	[`telegraf:1.27`](#telegraf127)
-	[`telegraf:1.27-alpine`](#telegraf127-alpine)
-	[`telegraf:1.27.4`](#telegraf1274)
-	[`telegraf:1.27.4-alpine`](#telegraf1274-alpine)
-	[`telegraf:1.28`](#telegraf128)
-	[`telegraf:1.28-alpine`](#telegraf128-alpine)
-	[`telegraf:1.28.4`](#telegraf1284)
-	[`telegraf:1.28.4-alpine`](#telegraf1284-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.26`

```console
$ docker pull telegraf@sha256:046b0ad200312b47e0bd31e20b9cc2a7578ad4ffa0e0634e8aa40e06770537fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.26` - linux; amd64

```console
$ docker pull telegraf@sha256:8a81d21346a98b5042873dc291c7af89ccc61dadc1fba3348030146d9392dde9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140137306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2877b6469bdbf3d10209af264812431d5febfd32393f2c8c46e28ca1a85acb61`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:59 GMT
ADD file:da3938f00f114fa8f5948fb7182da39c43e5ce57a334ba528681cb29aff0d2f6 in / 
# Wed, 01 Nov 2023 00:21:00 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:53:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 18:14:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 18:14:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 18:14:04 GMT
ENV TELEGRAF_VERSION=1.26.3
# Wed, 01 Nov 2023 18:14:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 01 Nov 2023 18:14:09 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 01 Nov 2023 18:14:09 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 01 Nov 2023 18:14:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 18:14:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2f088d622efd8dbaa13d01eafd0aac8f9f33bb335edd3be897ae8059338c7bf7`  
		Last Modified: Wed, 01 Nov 2023 00:25:49 GMT  
		Size: 55.1 MB (55058052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de448b80f06437f3025dcaa9285d40c9c81e4be00df1b04bd5a26fd6b9447fc8`  
		Last Modified: Wed, 01 Nov 2023 01:03:07 GMT  
		Size: 15.8 MB (15764212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c428699eca4887b50b52ca088033fc786969dae38254fa3f59d8c0b98559d00`  
		Last Modified: Wed, 01 Nov 2023 18:15:02 GMT  
		Size: 18.8 MB (18760403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ddfe4dbc6b3c33ba857e944b1d6856023a9d26aa847fdb27ee012ea1f304cd`  
		Last Modified: Wed, 01 Nov 2023 18:14:59 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bce5aa8d6ee1cbe8ebdfafc1f58e3c3ba002daa18ef9905d53066a2ce15f19`  
		Last Modified: Wed, 01 Nov 2023 18:15:07 GMT  
		Size: 50.6 MB (50552483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41270de5d27a6f5994aae4bb1b59d831dd773215983050637a0463f02cb835c3`  
		Last Modified: Wed, 01 Nov 2023 18:14:59 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.26` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:04422ac98dd80cda9a8d74de277dd6f9e1c7ce90173738bb30ff874f8a9600c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129842983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485e56ebc7c13ba0ca6367fb2652d815ef0a6bef2f4a250208ec0352fc746f2c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:58:01 GMT
ADD file:5e11ff51eeca3d0b7e760186b5792864fee2bfe7e8a1fa531a89870abaebfc89 in / 
# Wed, 01 Nov 2023 00:58:02 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:31:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 16:52:38 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 16:52:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 16:52:39 GMT
ENV TELEGRAF_VERSION=1.26.3
# Wed, 01 Nov 2023 16:52:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 01 Nov 2023 16:52:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 01 Nov 2023 16:52:47 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 01 Nov 2023 16:52:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 16:52:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:17b69ad2612f8fffb539ede3765dcc1fbd121518fd38fe89720482d622dbc960`  
		Last Modified: Wed, 01 Nov 2023 01:02:32 GMT  
		Size: 50.2 MB (50215350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0803d90cd63c47dea677f156a9802a95d09886d9a3b07415dd94b2ac199f25`  
		Last Modified: Wed, 01 Nov 2023 02:43:01 GMT  
		Size: 14.9 MB (14879723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837adaf75d17a3fa0c0dd192d54cb5b9ee3c951fba5dff4ecdf51b535782ff54`  
		Last Modified: Wed, 01 Nov 2023 16:53:41 GMT  
		Size: 17.5 MB (17463044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a804229723b26fee7d31e9b469be22fdcc1fe11da6caf653106e0c368b45382a`  
		Last Modified: Wed, 01 Nov 2023 16:53:38 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f05b4f0d33976825d45583a5a2ccbf92a9671f76c44ceaeab4a60ae772ff25`  
		Last Modified: Wed, 01 Nov 2023 16:53:47 GMT  
		Size: 47.3 MB (47282707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d3a381da390d6c5b80c0b2d38e84dda59c5b997b95e65054aa54ce40f228be`  
		Last Modified: Wed, 01 Nov 2023 16:53:38 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.26` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b19d71341be61bfcbf2bbc94f00528e5fd92533351c67808cc4b24c5c67a2ec8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134031146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed295b1706392f2776d65d1786cc438b6193e7bbf975cee2676fedc79aa5e64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:48 GMT
ADD file:f5677286e85ce6a345c7f5937e1ec576c37228e49c0fafe33574614c81cb7f76 in / 
# Wed, 01 Nov 2023 00:39:48 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:57 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 14:11:58 GMT
ENV TELEGRAF_VERSION=1.26.3
# Wed, 01 Nov 2023 14:12:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 01 Nov 2023 14:12:05 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 01 Nov 2023 14:12:05 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 01 Nov 2023 14:12:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 14:12:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d42ebdfc37acca5c3acbe173ac11133e691b402003a525c2b8431baf6935291e`  
		Last Modified: Wed, 01 Nov 2023 00:43:25 GMT  
		Size: 53.7 MB (53707757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098bcc814ee5bafa2842bc45ecc3974bc4f2b66d05b05a8da5ac0c9fb91be947`  
		Last Modified: Wed, 01 Nov 2023 02:14:42 GMT  
		Size: 15.7 MB (15749872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33088cbdc7f34ed8fca8fb738cc7e1301d82f11dc19f46c71e229916967589f1`  
		Last Modified: Wed, 01 Nov 2023 14:12:55 GMT  
		Size: 18.6 MB (18599536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ffc44414465ca6a2cd9395633a2778e59689332caf6fa94bc9f6f9b175f5b0`  
		Last Modified: Wed, 01 Nov 2023 14:12:52 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa1c3a0e1fa9c842bffc05bf277ce513a02a670237273e5ad26607559f05fdd`  
		Last Modified: Wed, 01 Nov 2023 14:12:58 GMT  
		Size: 46.0 MB (45971835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a45e0d6ac254ef12fdaba91ea9edd3a1714156e74dc51532a81da3b9b5c1a1`  
		Last Modified: Wed, 01 Nov 2023 14:12:53 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.26-alpine`

```console
$ docker pull telegraf@sha256:2fb0d7dcc11ab727d9e2e5b05c0ac82be740a22936117d76b9914f7a8df0959f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.26-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:cd6fdb97c35d23921c56ac02294bc74222cf7edb96064fa1b314f8e2fc630126
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56442971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65b8f7eed3acc3df20dedbd2c4de09c5a7b614822afa9fabe928ee01bf7f99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:29:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:41:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:41:36 GMT
ENV TELEGRAF_VERSION=1.26.3
# Sat, 21 Oct 2023 03:41:43 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:41:43 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:41:43 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:41:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:41:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b161763ec9e11116a97547438c5541153248aba5eddc76475885813812367da`  
		Last Modified: Tue, 17 Oct 2023 01:31:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce697a40ba666c0b939bdfff27ea7f13e38a2363f3ea3aacfd8d5d5aa7239a5`  
		Last Modified: Sat, 21 Oct 2023 03:42:33 GMT  
		Size: 2.7 MB (2671799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb68957bb0474b77a292c6f1875391f2fde9feeee846b9585aaf1b1784e905`  
		Last Modified: Sat, 21 Oct 2023 03:42:40 GMT  
		Size: 50.4 MB (50391960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb42df3bbacb302690503e1ab44cdae6eec964b9467d9d8d98f0c965cec1b102`  
		Last Modified: Sat, 21 Oct 2023 03:42:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.26-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:886ff7d38f0f58e105588b7098329984ef8e1d3c543649415c2150710676d31a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51775137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c79d58dc20ceb6d3890cb65eb511e3e18e20510aa6c2193ed12affd33b3ca3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 03:05:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:05:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:05:05 GMT
ENV TELEGRAF_VERSION=1.26.3
# Sat, 21 Oct 2023 03:05:15 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:05:16 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:05:16 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:05:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:05:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20cffce9f02c4faf5b734eac9c68df5443330a55a792e82a17d54196a5def44`  
		Last Modified: Sat, 21 Oct 2023 03:06:04 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995b550fd38b5dfc7dab42f13c3a28e8c9d6e08aaf414321bbf9b926e8bc47b3`  
		Last Modified: Sat, 21 Oct 2023 03:06:05 GMT  
		Size: 2.7 MB (2703935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aaa5e94e88830c33ad85ebe381728f95c9fba46a2f0b587a85ae055ac3ce7d`  
		Last Modified: Sat, 21 Oct 2023 03:06:09 GMT  
		Size: 45.8 MB (45812303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afdf42e99e6b76dcfc17aaacc7e3506486b18e712855245382746a6f298ba07`  
		Last Modified: Sat, 21 Oct 2023 03:06:04 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.26.3`

```console
$ docker pull telegraf@sha256:046b0ad200312b47e0bd31e20b9cc2a7578ad4ffa0e0634e8aa40e06770537fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.26.3` - linux; amd64

```console
$ docker pull telegraf@sha256:8a81d21346a98b5042873dc291c7af89ccc61dadc1fba3348030146d9392dde9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140137306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2877b6469bdbf3d10209af264812431d5febfd32393f2c8c46e28ca1a85acb61`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:59 GMT
ADD file:da3938f00f114fa8f5948fb7182da39c43e5ce57a334ba528681cb29aff0d2f6 in / 
# Wed, 01 Nov 2023 00:21:00 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:53:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 18:14:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 18:14:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 18:14:04 GMT
ENV TELEGRAF_VERSION=1.26.3
# Wed, 01 Nov 2023 18:14:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 01 Nov 2023 18:14:09 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 01 Nov 2023 18:14:09 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 01 Nov 2023 18:14:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 18:14:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2f088d622efd8dbaa13d01eafd0aac8f9f33bb335edd3be897ae8059338c7bf7`  
		Last Modified: Wed, 01 Nov 2023 00:25:49 GMT  
		Size: 55.1 MB (55058052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de448b80f06437f3025dcaa9285d40c9c81e4be00df1b04bd5a26fd6b9447fc8`  
		Last Modified: Wed, 01 Nov 2023 01:03:07 GMT  
		Size: 15.8 MB (15764212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c428699eca4887b50b52ca088033fc786969dae38254fa3f59d8c0b98559d00`  
		Last Modified: Wed, 01 Nov 2023 18:15:02 GMT  
		Size: 18.8 MB (18760403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ddfe4dbc6b3c33ba857e944b1d6856023a9d26aa847fdb27ee012ea1f304cd`  
		Last Modified: Wed, 01 Nov 2023 18:14:59 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bce5aa8d6ee1cbe8ebdfafc1f58e3c3ba002daa18ef9905d53066a2ce15f19`  
		Last Modified: Wed, 01 Nov 2023 18:15:07 GMT  
		Size: 50.6 MB (50552483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41270de5d27a6f5994aae4bb1b59d831dd773215983050637a0463f02cb835c3`  
		Last Modified: Wed, 01 Nov 2023 18:14:59 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.26.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:04422ac98dd80cda9a8d74de277dd6f9e1c7ce90173738bb30ff874f8a9600c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129842983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485e56ebc7c13ba0ca6367fb2652d815ef0a6bef2f4a250208ec0352fc746f2c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:58:01 GMT
ADD file:5e11ff51eeca3d0b7e760186b5792864fee2bfe7e8a1fa531a89870abaebfc89 in / 
# Wed, 01 Nov 2023 00:58:02 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:31:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 16:52:38 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 16:52:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 16:52:39 GMT
ENV TELEGRAF_VERSION=1.26.3
# Wed, 01 Nov 2023 16:52:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 01 Nov 2023 16:52:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 01 Nov 2023 16:52:47 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 01 Nov 2023 16:52:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 16:52:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:17b69ad2612f8fffb539ede3765dcc1fbd121518fd38fe89720482d622dbc960`  
		Last Modified: Wed, 01 Nov 2023 01:02:32 GMT  
		Size: 50.2 MB (50215350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0803d90cd63c47dea677f156a9802a95d09886d9a3b07415dd94b2ac199f25`  
		Last Modified: Wed, 01 Nov 2023 02:43:01 GMT  
		Size: 14.9 MB (14879723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837adaf75d17a3fa0c0dd192d54cb5b9ee3c951fba5dff4ecdf51b535782ff54`  
		Last Modified: Wed, 01 Nov 2023 16:53:41 GMT  
		Size: 17.5 MB (17463044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a804229723b26fee7d31e9b469be22fdcc1fe11da6caf653106e0c368b45382a`  
		Last Modified: Wed, 01 Nov 2023 16:53:38 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f05b4f0d33976825d45583a5a2ccbf92a9671f76c44ceaeab4a60ae772ff25`  
		Last Modified: Wed, 01 Nov 2023 16:53:47 GMT  
		Size: 47.3 MB (47282707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d3a381da390d6c5b80c0b2d38e84dda59c5b997b95e65054aa54ce40f228be`  
		Last Modified: Wed, 01 Nov 2023 16:53:38 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.26.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b19d71341be61bfcbf2bbc94f00528e5fd92533351c67808cc4b24c5c67a2ec8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134031146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed295b1706392f2776d65d1786cc438b6193e7bbf975cee2676fedc79aa5e64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:48 GMT
ADD file:f5677286e85ce6a345c7f5937e1ec576c37228e49c0fafe33574614c81cb7f76 in / 
# Wed, 01 Nov 2023 00:39:48 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:57 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:11:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 14:11:58 GMT
ENV TELEGRAF_VERSION=1.26.3
# Wed, 01 Nov 2023 14:12:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 01 Nov 2023 14:12:05 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 01 Nov 2023 14:12:05 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 01 Nov 2023 14:12:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 14:12:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d42ebdfc37acca5c3acbe173ac11133e691b402003a525c2b8431baf6935291e`  
		Last Modified: Wed, 01 Nov 2023 00:43:25 GMT  
		Size: 53.7 MB (53707757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098bcc814ee5bafa2842bc45ecc3974bc4f2b66d05b05a8da5ac0c9fb91be947`  
		Last Modified: Wed, 01 Nov 2023 02:14:42 GMT  
		Size: 15.7 MB (15749872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33088cbdc7f34ed8fca8fb738cc7e1301d82f11dc19f46c71e229916967589f1`  
		Last Modified: Wed, 01 Nov 2023 14:12:55 GMT  
		Size: 18.6 MB (18599536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ffc44414465ca6a2cd9395633a2778e59689332caf6fa94bc9f6f9b175f5b0`  
		Last Modified: Wed, 01 Nov 2023 14:12:52 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa1c3a0e1fa9c842bffc05bf277ce513a02a670237273e5ad26607559f05fdd`  
		Last Modified: Wed, 01 Nov 2023 14:12:58 GMT  
		Size: 46.0 MB (45971835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a45e0d6ac254ef12fdaba91ea9edd3a1714156e74dc51532a81da3b9b5c1a1`  
		Last Modified: Wed, 01 Nov 2023 14:12:53 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.26.3-alpine`

```console
$ docker pull telegraf@sha256:2fb0d7dcc11ab727d9e2e5b05c0ac82be740a22936117d76b9914f7a8df0959f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.26.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:cd6fdb97c35d23921c56ac02294bc74222cf7edb96064fa1b314f8e2fc630126
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56442971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65b8f7eed3acc3df20dedbd2c4de09c5a7b614822afa9fabe928ee01bf7f99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:29:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:41:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:41:36 GMT
ENV TELEGRAF_VERSION=1.26.3
# Sat, 21 Oct 2023 03:41:43 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:41:43 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:41:43 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:41:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:41:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b161763ec9e11116a97547438c5541153248aba5eddc76475885813812367da`  
		Last Modified: Tue, 17 Oct 2023 01:31:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce697a40ba666c0b939bdfff27ea7f13e38a2363f3ea3aacfd8d5d5aa7239a5`  
		Last Modified: Sat, 21 Oct 2023 03:42:33 GMT  
		Size: 2.7 MB (2671799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb68957bb0474b77a292c6f1875391f2fde9feeee846b9585aaf1b1784e905`  
		Last Modified: Sat, 21 Oct 2023 03:42:40 GMT  
		Size: 50.4 MB (50391960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb42df3bbacb302690503e1ab44cdae6eec964b9467d9d8d98f0c965cec1b102`  
		Last Modified: Sat, 21 Oct 2023 03:42:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.26.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:886ff7d38f0f58e105588b7098329984ef8e1d3c543649415c2150710676d31a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51775137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c79d58dc20ceb6d3890cb65eb511e3e18e20510aa6c2193ed12affd33b3ca3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 03:05:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:05:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:05:05 GMT
ENV TELEGRAF_VERSION=1.26.3
# Sat, 21 Oct 2023 03:05:15 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:05:16 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:05:16 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:05:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:05:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20cffce9f02c4faf5b734eac9c68df5443330a55a792e82a17d54196a5def44`  
		Last Modified: Sat, 21 Oct 2023 03:06:04 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995b550fd38b5dfc7dab42f13c3a28e8c9d6e08aaf414321bbf9b926e8bc47b3`  
		Last Modified: Sat, 21 Oct 2023 03:06:05 GMT  
		Size: 2.7 MB (2703935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aaa5e94e88830c33ad85ebe381728f95c9fba46a2f0b587a85ae055ac3ce7d`  
		Last Modified: Sat, 21 Oct 2023 03:06:09 GMT  
		Size: 45.8 MB (45812303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afdf42e99e6b76dcfc17aaacc7e3506486b18e712855245382746a6f298ba07`  
		Last Modified: Sat, 21 Oct 2023 03:06:04 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.27`

```console
$ docker pull telegraf@sha256:87b455146f962e2fe971daa2791a83842818eb5b459cfe086dbdab31da96aeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.27` - linux; amd64

```console
$ docker pull telegraf@sha256:9c9f073411e28f94491357d86b630c5d5a306fd44bb1eeefb68c40eb24ed8577
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148105707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3e994147f8420d6678c798530212c59dd80e0b2cb35ee7d5f8678e2934d404`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:37 GMT
ADD file:3e9b6405f11dd24ce62105c033f1d8b931d9409298553f63b03af1b6dd1dda35 in / 
# Wed, 01 Nov 2023 00:20:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:52:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 18:14:22 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 18:14:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 18:14:24 GMT
ENV TELEGRAF_VERSION=1.27.4
# Wed, 01 Nov 2023 18:14:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 01 Nov 2023 18:14:28 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 01 Nov 2023 18:14:28 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 01 Nov 2023 18:14:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 18:14:28 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8457fd5474e70835e4482983a5662355d892d5f6f0f90a27a8e9f009997e8196`  
		Last Modified: Wed, 01 Nov 2023 00:25:05 GMT  
		Size: 49.6 MB (49582024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13baa2029dde87a21b87127168a0fb50a007c07da6b5adc8864e1fe1376c86ff`  
		Last Modified: Wed, 01 Nov 2023 01:02:01 GMT  
		Size: 24.0 MB (24049147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb5cbba93e421136061ff7a287eca07e2c44834e732791ce0db133784207ea7`  
		Last Modified: Wed, 01 Nov 2023 18:15:20 GMT  
		Size: 19.1 MB (19145622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2a9cce78837515beeedadd4ef39d88e074358603c1c6360199c5bbb54a9356`  
		Last Modified: Wed, 01 Nov 2023 18:15:17 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a64261637e9cd24458d2e657a315be01a4ec6ab0548769414ff58ab9838a146`  
		Last Modified: Wed, 01 Nov 2023 18:15:27 GMT  
		Size: 55.3 MB (55326769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bff36b9725d1b7ad1108776f4d329d467ffde5c2e9399cbea1d7de371a7ba7`  
		Last Modified: Wed, 01 Nov 2023 18:15:17 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:cbb9dcc76a44d6b61664511a160e5ce362d12470731a6cadf5405eb34c46ae2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136630853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53b808b6e144a465e0e31140ed409c194d19c5da59580d7903123461f4f5450`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:42 GMT
ADD file:3b2b4eda35d794b39d6b5567e81651625af51da3deb3f63b3ffdffa07720646e in / 
# Wed, 01 Nov 2023 00:57:42 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:30:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 16:53:02 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 16:53:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 16:53:04 GMT
ENV TELEGRAF_VERSION=1.27.4
# Wed, 01 Nov 2023 16:53:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 01 Nov 2023 16:53:13 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 01 Nov 2023 16:53:13 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 01 Nov 2023 16:53:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 16:53:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9bf855396a6f46c1cbac4e188af10f2c38474f989707b0b1b406b48c4b7284ef`  
		Last Modified: Wed, 01 Nov 2023 01:01:41 GMT  
		Size: 45.2 MB (45179410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6e59eca644b227cb755978679a3031e7b3f9a5c707057c293f2ba8732d8ef2`  
		Last Modified: Wed, 01 Nov 2023 02:41:40 GMT  
		Size: 22.0 MB (21951880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce8fce53d3efe8a2a390487834b7740bd7e15c9881525b32ef88c1042a1f6dd`  
		Last Modified: Wed, 01 Nov 2023 16:54:00 GMT  
		Size: 18.0 MB (17991623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c85606ced42864565ce1f0bdc077764bb9239e718d2786f778966cd9f1ff659`  
		Last Modified: Wed, 01 Nov 2023 16:53:56 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ff1c23c62e68181a6f019f7eca1c49c510d2967723e0da8941857af45c83fe`  
		Last Modified: Wed, 01 Nov 2023 16:54:05 GMT  
		Size: 51.5 MB (51505798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54fa77b4f11c9765bed0d8f97e27394ca2f834bae3e358d03fc2c70577bd395`  
		Last Modified: Wed, 01 Nov 2023 16:53:56 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d375e9982ac23181614f2b499e4321f14803c72bbd503ad7f59f5def25f0d095
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142237084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d38ecb432323ced66e65cf7d71f2c912bb6bba276257d84d0f907cdd3270f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:04:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:12:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:12:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 14:12:19 GMT
ENV TELEGRAF_VERSION=1.27.4
# Wed, 01 Nov 2023 14:12:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 01 Nov 2023 14:12:24 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 01 Nov 2023 14:12:24 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 01 Nov 2023 14:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 14:12:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d826ee8aa65e56e167f0e27fa65cfc065687a7ac6c360787d5940d8b51f0cf1`  
		Last Modified: Wed, 01 Nov 2023 02:13:39 GMT  
		Size: 23.6 MB (23584896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2794f9c6546f6aa0a9a29e1eab9226f3bc5b9ba469b98cd8850edb9209ee4be2`  
		Last Modified: Wed, 01 Nov 2023 14:13:11 GMT  
		Size: 19.1 MB (19078763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916aaf6834f48574720db24d78a45050d28210cadfdba1f7e5b8952d05bae145`  
		Last Modified: Wed, 01 Nov 2023 14:13:09 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72005c3fdf755c671fb5adcb69289940a8743640321a5b6332a2f872a7e6c494`  
		Last Modified: Wed, 01 Nov 2023 14:13:15 GMT  
		Size: 50.0 MB (49958613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50786f3554ebf9ad42d4ed694fa6f1ec6c0521c0aeeee5fc7893bdd8cd5f2cf`  
		Last Modified: Wed, 01 Nov 2023 14:13:09 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.27-alpine`

```console
$ docker pull telegraf@sha256:f77ed7dddb02a84b5bdd31d9f89a018ee08edea598b7da9dd81e5d66577f651b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.27-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:6eccd860212b44034872f6130348edf970d72a900afcbafd229208de4d29b9d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61199653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48fd08420a9d1b3991e3781cda8fb3b5c38d0211c2fef5fef53881f9389ef80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:30:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:41:50 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:41:50 GMT
ENV TELEGRAF_VERSION=1.27.4
# Sat, 21 Oct 2023 03:42:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:42:01 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:42:01 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:42:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:42:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5352bf3aec614dde8ac36d38f28f5021eff4c2ff0226eb22dfa667f2b2add1`  
		Last Modified: Tue, 17 Oct 2023 01:33:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba00d64dccafdbc853dd8b93a8277f727ce3f033368e6501a6bd8e5d8146745a`  
		Last Modified: Sat, 21 Oct 2023 03:42:51 GMT  
		Size: 2.6 MB (2644972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450dcdf691f11f970afef73d942c63e6161a568b77622ff4107e6478725af37c`  
		Last Modified: Sat, 21 Oct 2023 03:42:59 GMT  
		Size: 55.2 MB (55152107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102b1a74ea9501518451d0ae11db2bee8fe1b66599de184e0ea725f93b37782e`  
		Last Modified: Sat, 21 Oct 2023 03:42:50 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b4e52a8cd5440d35e1009c242974397bdcc55a2a50066ed33ab4fddcc7e01b93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55801017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d412a0494e0a1ec188214fe6a98c9bad9ded0972205b6354751f16585a8e3f3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 00:43:51 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:05:22 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:05:22 GMT
ENV TELEGRAF_VERSION=1.27.4
# Sat, 21 Oct 2023 03:05:31 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:05:32 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:05:32 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:05:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:05:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e248ba14d9e254569a72ce1316c31cb26327474bc388ccd8fbd2fa78078db3aa`  
		Last Modified: Tue, 17 Oct 2023 00:44:22 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f9000c980c4ebf3511e8960492d4efd4c2527f058385ee1575fdb80c0cea7`  
		Last Modified: Sat, 21 Oct 2023 03:06:20 GMT  
		Size: 2.7 MB (2673194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ef6f17a9a0ea6e7a97c008cc018d7359892e7edc9648fa9028a0c8f9ca1174`  
		Last Modified: Sat, 21 Oct 2023 03:06:25 GMT  
		Size: 49.8 MB (49795386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab157c6d650bcef23423e9caf5874f8b88eab7ddf83f54c5acd6e656238c20a`  
		Last Modified: Sat, 21 Oct 2023 03:06:19 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.27.4`

```console
$ docker pull telegraf@sha256:87b455146f962e2fe971daa2791a83842818eb5b459cfe086dbdab31da96aeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.27.4` - linux; amd64

```console
$ docker pull telegraf@sha256:9c9f073411e28f94491357d86b630c5d5a306fd44bb1eeefb68c40eb24ed8577
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148105707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3e994147f8420d6678c798530212c59dd80e0b2cb35ee7d5f8678e2934d404`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:37 GMT
ADD file:3e9b6405f11dd24ce62105c033f1d8b931d9409298553f63b03af1b6dd1dda35 in / 
# Wed, 01 Nov 2023 00:20:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:52:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 18:14:22 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 18:14:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 18:14:24 GMT
ENV TELEGRAF_VERSION=1.27.4
# Wed, 01 Nov 2023 18:14:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 01 Nov 2023 18:14:28 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 01 Nov 2023 18:14:28 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 01 Nov 2023 18:14:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 18:14:28 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8457fd5474e70835e4482983a5662355d892d5f6f0f90a27a8e9f009997e8196`  
		Last Modified: Wed, 01 Nov 2023 00:25:05 GMT  
		Size: 49.6 MB (49582024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13baa2029dde87a21b87127168a0fb50a007c07da6b5adc8864e1fe1376c86ff`  
		Last Modified: Wed, 01 Nov 2023 01:02:01 GMT  
		Size: 24.0 MB (24049147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb5cbba93e421136061ff7a287eca07e2c44834e732791ce0db133784207ea7`  
		Last Modified: Wed, 01 Nov 2023 18:15:20 GMT  
		Size: 19.1 MB (19145622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2a9cce78837515beeedadd4ef39d88e074358603c1c6360199c5bbb54a9356`  
		Last Modified: Wed, 01 Nov 2023 18:15:17 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a64261637e9cd24458d2e657a315be01a4ec6ab0548769414ff58ab9838a146`  
		Last Modified: Wed, 01 Nov 2023 18:15:27 GMT  
		Size: 55.3 MB (55326769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bff36b9725d1b7ad1108776f4d329d467ffde5c2e9399cbea1d7de371a7ba7`  
		Last Modified: Wed, 01 Nov 2023 18:15:17 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:cbb9dcc76a44d6b61664511a160e5ce362d12470731a6cadf5405eb34c46ae2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136630853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53b808b6e144a465e0e31140ed409c194d19c5da59580d7903123461f4f5450`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:42 GMT
ADD file:3b2b4eda35d794b39d6b5567e81651625af51da3deb3f63b3ffdffa07720646e in / 
# Wed, 01 Nov 2023 00:57:42 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:30:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 16:53:02 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 16:53:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 16:53:04 GMT
ENV TELEGRAF_VERSION=1.27.4
# Wed, 01 Nov 2023 16:53:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 01 Nov 2023 16:53:13 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 01 Nov 2023 16:53:13 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 01 Nov 2023 16:53:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 16:53:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9bf855396a6f46c1cbac4e188af10f2c38474f989707b0b1b406b48c4b7284ef`  
		Last Modified: Wed, 01 Nov 2023 01:01:41 GMT  
		Size: 45.2 MB (45179410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6e59eca644b227cb755978679a3031e7b3f9a5c707057c293f2ba8732d8ef2`  
		Last Modified: Wed, 01 Nov 2023 02:41:40 GMT  
		Size: 22.0 MB (21951880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce8fce53d3efe8a2a390487834b7740bd7e15c9881525b32ef88c1042a1f6dd`  
		Last Modified: Wed, 01 Nov 2023 16:54:00 GMT  
		Size: 18.0 MB (17991623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c85606ced42864565ce1f0bdc077764bb9239e718d2786f778966cd9f1ff659`  
		Last Modified: Wed, 01 Nov 2023 16:53:56 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ff1c23c62e68181a6f019f7eca1c49c510d2967723e0da8941857af45c83fe`  
		Last Modified: Wed, 01 Nov 2023 16:54:05 GMT  
		Size: 51.5 MB (51505798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54fa77b4f11c9765bed0d8f97e27394ca2f834bae3e358d03fc2c70577bd395`  
		Last Modified: Wed, 01 Nov 2023 16:53:56 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:d375e9982ac23181614f2b499e4321f14803c72bbd503ad7f59f5def25f0d095
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142237084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d38ecb432323ced66e65cf7d71f2c912bb6bba276257d84d0f907cdd3270f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:04:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:12:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:12:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 14:12:19 GMT
ENV TELEGRAF_VERSION=1.27.4
# Wed, 01 Nov 2023 14:12:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 01 Nov 2023 14:12:24 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 01 Nov 2023 14:12:24 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 01 Nov 2023 14:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 14:12:24 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d826ee8aa65e56e167f0e27fa65cfc065687a7ac6c360787d5940d8b51f0cf1`  
		Last Modified: Wed, 01 Nov 2023 02:13:39 GMT  
		Size: 23.6 MB (23584896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2794f9c6546f6aa0a9a29e1eab9226f3bc5b9ba469b98cd8850edb9209ee4be2`  
		Last Modified: Wed, 01 Nov 2023 14:13:11 GMT  
		Size: 19.1 MB (19078763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916aaf6834f48574720db24d78a45050d28210cadfdba1f7e5b8952d05bae145`  
		Last Modified: Wed, 01 Nov 2023 14:13:09 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72005c3fdf755c671fb5adcb69289940a8743640321a5b6332a2f872a7e6c494`  
		Last Modified: Wed, 01 Nov 2023 14:13:15 GMT  
		Size: 50.0 MB (49958613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50786f3554ebf9ad42d4ed694fa6f1ec6c0521c0aeeee5fc7893bdd8cd5f2cf`  
		Last Modified: Wed, 01 Nov 2023 14:13:09 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.27.4-alpine`

```console
$ docker pull telegraf@sha256:f77ed7dddb02a84b5bdd31d9f89a018ee08edea598b7da9dd81e5d66577f651b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.27.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:6eccd860212b44034872f6130348edf970d72a900afcbafd229208de4d29b9d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61199653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48fd08420a9d1b3991e3781cda8fb3b5c38d0211c2fef5fef53881f9389ef80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:30:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:41:50 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:41:50 GMT
ENV TELEGRAF_VERSION=1.27.4
# Sat, 21 Oct 2023 03:42:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:42:01 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:42:01 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:42:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:42:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5352bf3aec614dde8ac36d38f28f5021eff4c2ff0226eb22dfa667f2b2add1`  
		Last Modified: Tue, 17 Oct 2023 01:33:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba00d64dccafdbc853dd8b93a8277f727ce3f033368e6501a6bd8e5d8146745a`  
		Last Modified: Sat, 21 Oct 2023 03:42:51 GMT  
		Size: 2.6 MB (2644972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450dcdf691f11f970afef73d942c63e6161a568b77622ff4107e6478725af37c`  
		Last Modified: Sat, 21 Oct 2023 03:42:59 GMT  
		Size: 55.2 MB (55152107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102b1a74ea9501518451d0ae11db2bee8fe1b66599de184e0ea725f93b37782e`  
		Last Modified: Sat, 21 Oct 2023 03:42:50 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b4e52a8cd5440d35e1009c242974397bdcc55a2a50066ed33ab4fddcc7e01b93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55801017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d412a0494e0a1ec188214fe6a98c9bad9ded0972205b6354751f16585a8e3f3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 00:43:51 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:05:22 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:05:22 GMT
ENV TELEGRAF_VERSION=1.27.4
# Sat, 21 Oct 2023 03:05:31 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:05:32 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:05:32 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:05:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:05:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e248ba14d9e254569a72ce1316c31cb26327474bc388ccd8fbd2fa78078db3aa`  
		Last Modified: Tue, 17 Oct 2023 00:44:22 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f9000c980c4ebf3511e8960492d4efd4c2527f058385ee1575fdb80c0cea7`  
		Last Modified: Sat, 21 Oct 2023 03:06:20 GMT  
		Size: 2.7 MB (2673194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ef6f17a9a0ea6e7a97c008cc018d7359892e7edc9648fa9028a0c8f9ca1174`  
		Last Modified: Sat, 21 Oct 2023 03:06:25 GMT  
		Size: 49.8 MB (49795386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab157c6d650bcef23423e9caf5874f8b88eab7ddf83f54c5acd6e656238c20a`  
		Last Modified: Sat, 21 Oct 2023 03:06:19 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28`

```console
$ docker pull telegraf@sha256:76fc78c61981f351fbf1b7fc4de77c03279f4d9a1738ad958be32bdacfc8b6dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.28` - linux; amd64

```console
$ docker pull telegraf@sha256:7bc2289a357d69032e5ebbed59e7a87d55cf4919612371a2de18f68cdf00f9f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149966520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbfde28aaccda5ac2ae975536d4deb9209610655d8f30d244cd546347ef5b8b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:37 GMT
ADD file:3e9b6405f11dd24ce62105c033f1d8b931d9409298553f63b03af1b6dd1dda35 in / 
# Wed, 01 Nov 2023 00:20:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:52:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 18:14:22 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 18:14:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 18:14:34 GMT
ENV TELEGRAF_VERSION=1.28.3
# Wed, 01 Nov 2023 18:14:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 01 Nov 2023 18:14:39 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 01 Nov 2023 18:14:39 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 01 Nov 2023 18:14:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 18:14:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8457fd5474e70835e4482983a5662355d892d5f6f0f90a27a8e9f009997e8196`  
		Last Modified: Wed, 01 Nov 2023 00:25:05 GMT  
		Size: 49.6 MB (49582024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13baa2029dde87a21b87127168a0fb50a007c07da6b5adc8864e1fe1376c86ff`  
		Last Modified: Wed, 01 Nov 2023 01:02:01 GMT  
		Size: 24.0 MB (24049147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb5cbba93e421136061ff7a287eca07e2c44834e732791ce0db133784207ea7`  
		Last Modified: Wed, 01 Nov 2023 18:15:20 GMT  
		Size: 19.1 MB (19145622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2a9cce78837515beeedadd4ef39d88e074358603c1c6360199c5bbb54a9356`  
		Last Modified: Wed, 01 Nov 2023 18:15:17 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e55f654019c0ee9812ae40e3b155dbe19a64fd834452145253773731365d1e`  
		Last Modified: Wed, 01 Nov 2023 18:15:47 GMT  
		Size: 57.2 MB (57187581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab4ee17986ebff94888c85d9c4e629c4217288d885d53243b28824e10f26e78`  
		Last Modified: Wed, 01 Nov 2023 18:15:38 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:1bded8b278b6144043f194e3813188af608aad4e3aef15254b84cc7469345a85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137770216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2764fe1ecd985363a74c3d1284a796d37780533e59e139acef71ccb5864d4aec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:42 GMT
ADD file:3b2b4eda35d794b39d6b5567e81651625af51da3deb3f63b3ffdffa07720646e in / 
# Wed, 01 Nov 2023 00:57:42 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:30:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 16:53:02 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 16:53:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 16:53:15 GMT
ENV TELEGRAF_VERSION=1.28.3
# Wed, 01 Nov 2023 16:53:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 01 Nov 2023 16:53:25 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 01 Nov 2023 16:53:25 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 01 Nov 2023 16:53:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 16:53:25 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9bf855396a6f46c1cbac4e188af10f2c38474f989707b0b1b406b48c4b7284ef`  
		Last Modified: Wed, 01 Nov 2023 01:01:41 GMT  
		Size: 45.2 MB (45179410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6e59eca644b227cb755978679a3031e7b3f9a5c707057c293f2ba8732d8ef2`  
		Last Modified: Wed, 01 Nov 2023 02:41:40 GMT  
		Size: 22.0 MB (21951880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce8fce53d3efe8a2a390487834b7740bd7e15c9881525b32ef88c1042a1f6dd`  
		Last Modified: Wed, 01 Nov 2023 16:54:00 GMT  
		Size: 18.0 MB (17991623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c85606ced42864565ce1f0bdc077764bb9239e718d2786f778966cd9f1ff659`  
		Last Modified: Wed, 01 Nov 2023 16:53:56 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaadbcfe854240109add9e8511c35a3504f784be99f55d7a3314df31cd42a829`  
		Last Modified: Wed, 01 Nov 2023 16:54:28 GMT  
		Size: 52.6 MB (52645159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca03ed8306b82e25c13d0f22b297160f872a849a8de4edc20a81fe37d4e20ae`  
		Last Modified: Wed, 01 Nov 2023 16:54:14 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:fbc1db28c1023e429f5e39883bea189bf03fb587acd20f45cd8b083f69dffeb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144116048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ea8a18cd17cd0bb73dc5757b615fd43885a5e649df086685e5e5fe770447a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:04:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:12:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:12:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 14:12:30 GMT
ENV TELEGRAF_VERSION=1.28.3
# Wed, 01 Nov 2023 14:12:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 01 Nov 2023 14:12:35 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 01 Nov 2023 14:12:35 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 01 Nov 2023 14:12:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 14:12:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d826ee8aa65e56e167f0e27fa65cfc065687a7ac6c360787d5940d8b51f0cf1`  
		Last Modified: Wed, 01 Nov 2023 02:13:39 GMT  
		Size: 23.6 MB (23584896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2794f9c6546f6aa0a9a29e1eab9226f3bc5b9ba469b98cd8850edb9209ee4be2`  
		Last Modified: Wed, 01 Nov 2023 14:13:11 GMT  
		Size: 19.1 MB (19078763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916aaf6834f48574720db24d78a45050d28210cadfdba1f7e5b8952d05bae145`  
		Last Modified: Wed, 01 Nov 2023 14:13:09 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d7817006e4ff14bbb97c4b4cf080d0c9f4e25d55a8045b7c8743f8753ed861`  
		Last Modified: Wed, 01 Nov 2023 14:13:31 GMT  
		Size: 51.8 MB (51837576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c0866c4d2cff249b3f424510031d574abfdd63537ae788278927423daeaeca`  
		Last Modified: Wed, 01 Nov 2023 14:13:25 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28-alpine`

```console
$ docker pull telegraf@sha256:0397dfc014179599ebfffe5b4cd4c275aeddfe4591b4e5940651667c96f8eff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.28-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9a7707e2d08ec455ce6706f056de5e9c01d0986a684dc6550c20cfc4b71afdf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63060864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0164f053a1414dce5b7a645eb1a55084d143d99557e514c72389c3e4a028c080`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:30:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:41:50 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 23 Oct 2023 23:27:19 GMT
ENV TELEGRAF_VERSION=1.28.3
# Mon, 23 Oct 2023 23:27:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 23 Oct 2023 23:27:26 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 23 Oct 2023 23:27:26 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 23 Oct 2023 23:27:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Oct 2023 23:27:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5352bf3aec614dde8ac36d38f28f5021eff4c2ff0226eb22dfa667f2b2add1`  
		Last Modified: Tue, 17 Oct 2023 01:33:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba00d64dccafdbc853dd8b93a8277f727ce3f033368e6501a6bd8e5d8146745a`  
		Last Modified: Sat, 21 Oct 2023 03:42:51 GMT  
		Size: 2.6 MB (2644972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e593ebf573ca536156bdddfcb78545a2a9550b06b4999fda0969ae6fb88e28b`  
		Last Modified: Mon, 23 Oct 2023 23:28:12 GMT  
		Size: 57.0 MB (57013318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fd50397242c6bb879f255cd7d82bc171608f1fc31c9e07e1f90a2fe9120f11`  
		Last Modified: Mon, 23 Oct 2023 23:28:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:593481616e589f58fb6ec5013911c9a67cd897effa8c3af84c9e2aae42b73774
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57673864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4dc2f0a847b07c1abd0083f5cdee87e7aa455c96125123d4f49cccbc1f0686`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 00:43:51 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:05:22 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 23 Oct 2023 23:55:10 GMT
ENV TELEGRAF_VERSION=1.28.3
# Mon, 23 Oct 2023 23:55:16 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 23 Oct 2023 23:55:17 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 23 Oct 2023 23:55:18 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 23 Oct 2023 23:55:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Oct 2023 23:55:18 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e248ba14d9e254569a72ce1316c31cb26327474bc388ccd8fbd2fa78078db3aa`  
		Last Modified: Tue, 17 Oct 2023 00:44:22 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f9000c980c4ebf3511e8960492d4efd4c2527f058385ee1575fdb80c0cea7`  
		Last Modified: Sat, 21 Oct 2023 03:06:20 GMT  
		Size: 2.7 MB (2673194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6345250d1f89ef0f22bf625ad5a3f61f102a7581b6c7d3d860fde2041a4e26ee`  
		Last Modified: Mon, 23 Oct 2023 23:56:00 GMT  
		Size: 51.7 MB (51668234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060a9ffb0b3a1bfabbcd2c3c8f73583178ef9ee11dc115c7d879700efcea73d9`  
		Last Modified: Mon, 23 Oct 2023 23:55:54 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28.4`

**does not exist** (yet?)

## `telegraf:1.28.4-alpine`

**does not exist** (yet?)

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:0397dfc014179599ebfffe5b4cd4c275aeddfe4591b4e5940651667c96f8eff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9a7707e2d08ec455ce6706f056de5e9c01d0986a684dc6550c20cfc4b71afdf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63060864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0164f053a1414dce5b7a645eb1a55084d143d99557e514c72389c3e4a028c080`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:30:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:41:50 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 23 Oct 2023 23:27:19 GMT
ENV TELEGRAF_VERSION=1.28.3
# Mon, 23 Oct 2023 23:27:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 23 Oct 2023 23:27:26 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 23 Oct 2023 23:27:26 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 23 Oct 2023 23:27:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Oct 2023 23:27:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5352bf3aec614dde8ac36d38f28f5021eff4c2ff0226eb22dfa667f2b2add1`  
		Last Modified: Tue, 17 Oct 2023 01:33:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba00d64dccafdbc853dd8b93a8277f727ce3f033368e6501a6bd8e5d8146745a`  
		Last Modified: Sat, 21 Oct 2023 03:42:51 GMT  
		Size: 2.6 MB (2644972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e593ebf573ca536156bdddfcb78545a2a9550b06b4999fda0969ae6fb88e28b`  
		Last Modified: Mon, 23 Oct 2023 23:28:12 GMT  
		Size: 57.0 MB (57013318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fd50397242c6bb879f255cd7d82bc171608f1fc31c9e07e1f90a2fe9120f11`  
		Last Modified: Mon, 23 Oct 2023 23:28:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:593481616e589f58fb6ec5013911c9a67cd897effa8c3af84c9e2aae42b73774
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57673864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4dc2f0a847b07c1abd0083f5cdee87e7aa455c96125123d4f49cccbc1f0686`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 00:43:51 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:05:22 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 23 Oct 2023 23:55:10 GMT
ENV TELEGRAF_VERSION=1.28.3
# Mon, 23 Oct 2023 23:55:16 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 23 Oct 2023 23:55:17 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 23 Oct 2023 23:55:18 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 23 Oct 2023 23:55:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Oct 2023 23:55:18 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e248ba14d9e254569a72ce1316c31cb26327474bc388ccd8fbd2fa78078db3aa`  
		Last Modified: Tue, 17 Oct 2023 00:44:22 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f9000c980c4ebf3511e8960492d4efd4c2527f058385ee1575fdb80c0cea7`  
		Last Modified: Sat, 21 Oct 2023 03:06:20 GMT  
		Size: 2.7 MB (2673194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6345250d1f89ef0f22bf625ad5a3f61f102a7581b6c7d3d860fde2041a4e26ee`  
		Last Modified: Mon, 23 Oct 2023 23:56:00 GMT  
		Size: 51.7 MB (51668234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060a9ffb0b3a1bfabbcd2c3c8f73583178ef9ee11dc115c7d879700efcea73d9`  
		Last Modified: Mon, 23 Oct 2023 23:55:54 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:76fc78c61981f351fbf1b7fc4de77c03279f4d9a1738ad958be32bdacfc8b6dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:7bc2289a357d69032e5ebbed59e7a87d55cf4919612371a2de18f68cdf00f9f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149966520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbfde28aaccda5ac2ae975536d4deb9209610655d8f30d244cd546347ef5b8b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:37 GMT
ADD file:3e9b6405f11dd24ce62105c033f1d8b931d9409298553f63b03af1b6dd1dda35 in / 
# Wed, 01 Nov 2023 00:20:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:52:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 18:14:22 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 18:14:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 18:14:34 GMT
ENV TELEGRAF_VERSION=1.28.3
# Wed, 01 Nov 2023 18:14:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 01 Nov 2023 18:14:39 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 01 Nov 2023 18:14:39 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 01 Nov 2023 18:14:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 18:14:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8457fd5474e70835e4482983a5662355d892d5f6f0f90a27a8e9f009997e8196`  
		Last Modified: Wed, 01 Nov 2023 00:25:05 GMT  
		Size: 49.6 MB (49582024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13baa2029dde87a21b87127168a0fb50a007c07da6b5adc8864e1fe1376c86ff`  
		Last Modified: Wed, 01 Nov 2023 01:02:01 GMT  
		Size: 24.0 MB (24049147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb5cbba93e421136061ff7a287eca07e2c44834e732791ce0db133784207ea7`  
		Last Modified: Wed, 01 Nov 2023 18:15:20 GMT  
		Size: 19.1 MB (19145622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2a9cce78837515beeedadd4ef39d88e074358603c1c6360199c5bbb54a9356`  
		Last Modified: Wed, 01 Nov 2023 18:15:17 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e55f654019c0ee9812ae40e3b155dbe19a64fd834452145253773731365d1e`  
		Last Modified: Wed, 01 Nov 2023 18:15:47 GMT  
		Size: 57.2 MB (57187581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab4ee17986ebff94888c85d9c4e629c4217288d885d53243b28824e10f26e78`  
		Last Modified: Wed, 01 Nov 2023 18:15:38 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:1bded8b278b6144043f194e3813188af608aad4e3aef15254b84cc7469345a85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137770216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2764fe1ecd985363a74c3d1284a796d37780533e59e139acef71ccb5864d4aec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:42 GMT
ADD file:3b2b4eda35d794b39d6b5567e81651625af51da3deb3f63b3ffdffa07720646e in / 
# Wed, 01 Nov 2023 00:57:42 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:30:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 16:53:02 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 16:53:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 16:53:15 GMT
ENV TELEGRAF_VERSION=1.28.3
# Wed, 01 Nov 2023 16:53:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 01 Nov 2023 16:53:25 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 01 Nov 2023 16:53:25 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 01 Nov 2023 16:53:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 16:53:25 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9bf855396a6f46c1cbac4e188af10f2c38474f989707b0b1b406b48c4b7284ef`  
		Last Modified: Wed, 01 Nov 2023 01:01:41 GMT  
		Size: 45.2 MB (45179410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6e59eca644b227cb755978679a3031e7b3f9a5c707057c293f2ba8732d8ef2`  
		Last Modified: Wed, 01 Nov 2023 02:41:40 GMT  
		Size: 22.0 MB (21951880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce8fce53d3efe8a2a390487834b7740bd7e15c9881525b32ef88c1042a1f6dd`  
		Last Modified: Wed, 01 Nov 2023 16:54:00 GMT  
		Size: 18.0 MB (17991623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c85606ced42864565ce1f0bdc077764bb9239e718d2786f778966cd9f1ff659`  
		Last Modified: Wed, 01 Nov 2023 16:53:56 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaadbcfe854240109add9e8511c35a3504f784be99f55d7a3314df31cd42a829`  
		Last Modified: Wed, 01 Nov 2023 16:54:28 GMT  
		Size: 52.6 MB (52645159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca03ed8306b82e25c13d0f22b297160f872a849a8de4edc20a81fe37d4e20ae`  
		Last Modified: Wed, 01 Nov 2023 16:54:14 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:fbc1db28c1023e429f5e39883bea189bf03fb587acd20f45cd8b083f69dffeb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144116048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ea8a18cd17cd0bb73dc5757b615fd43885a5e649df086685e5e5fe770447a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:04:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:12:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:12:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 01 Nov 2023 14:12:30 GMT
ENV TELEGRAF_VERSION=1.28.3
# Wed, 01 Nov 2023 14:12:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 01 Nov 2023 14:12:35 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 01 Nov 2023 14:12:35 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 01 Nov 2023 14:12:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Nov 2023 14:12:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d826ee8aa65e56e167f0e27fa65cfc065687a7ac6c360787d5940d8b51f0cf1`  
		Last Modified: Wed, 01 Nov 2023 02:13:39 GMT  
		Size: 23.6 MB (23584896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2794f9c6546f6aa0a9a29e1eab9226f3bc5b9ba469b98cd8850edb9209ee4be2`  
		Last Modified: Wed, 01 Nov 2023 14:13:11 GMT  
		Size: 19.1 MB (19078763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916aaf6834f48574720db24d78a45050d28210cadfdba1f7e5b8952d05bae145`  
		Last Modified: Wed, 01 Nov 2023 14:13:09 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d7817006e4ff14bbb97c4b4cf080d0c9f4e25d55a8045b7c8743f8753ed861`  
		Last Modified: Wed, 01 Nov 2023 14:13:31 GMT  
		Size: 51.8 MB (51837576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c0866c4d2cff249b3f424510031d574abfdd63537ae788278927423daeaeca`  
		Last Modified: Wed, 01 Nov 2023 14:13:25 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
