## `telegraf:latest`

```console
$ docker pull telegraf@sha256:7aec0ff809c5f5cfe6c17de2eab0f72b82cc9dc2124b920256381e593ad0ec08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:526d397c104c73ff8aacb3e7c6cfae7cb0da7e01a197755cd171553ffc1df6fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131486479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a228d15d8f171fe6867bbc216708fb46b90cbdc53f628a5ef23b6d367d1fe508`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:16 GMT
ADD file:798015650079cb88614ff181a30f9c3d3fde8361c49ae2dec2058d5a3e61f5df in / 
# Thu, 23 Jun 2022 00:20:16 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:50:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:50:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 15:34:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 15:34:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Jul 2022 00:14:22 GMT
ENV TELEGRAF_VERSION=1.23.2
# Tue, 12 Jul 2022 00:14:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 12 Jul 2022 00:14:27 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 12 Jul 2022 00:14:27 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Tue, 12 Jul 2022 00:14:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jul 2022 00:14:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1339eaac5b67d16d6d9f41fb7a7b96f7cebf3ba4beab36cbb60935aa772af583`  
		Last Modified: Thu, 23 Jun 2022 00:24:48 GMT  
		Size: 55.0 MB (55009886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c78fa1b97999d08408734a61040475ade5bd7e33e91c0d5170dba2c7c7a92fd`  
		Last Modified: Thu, 23 Jun 2022 00:58:38 GMT  
		Size: 5.2 MB (5155961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f0d2bd524377dc42d072443c0e5e7cafa14f5df609d39bb1f717f43817a2cd`  
		Last Modified: Thu, 23 Jun 2022 00:58:38 GMT  
		Size: 10.9 MB (10875087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4a1c3e9297531b81773c0410c9d2677cd96b90cda2b88f4639ee14487a049a`  
		Last Modified: Thu, 23 Jun 2022 15:35:27 GMT  
		Size: 18.8 MB (18760241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff261e1b93000aaba9f941e3a3aef0c2912c27b6dff5f57d3fa96f80cbd5cb7d`  
		Last Modified: Thu, 23 Jun 2022 15:35:24 GMT  
		Size: 2.9 KB (2898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1c4db65ee26602a6565d94bd92bbee509adc1f148398b6337ac722d499356c`  
		Last Modified: Tue, 12 Jul 2022 00:15:05 GMT  
		Size: 41.7 MB (41682062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c262b725fc4fa91b8eb28991460cbbd7866b301d8cb28d426b2e49b072ee3c7`  
		Last Modified: Tue, 12 Jul 2022 00:14:58 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:9aa9773f5a5e48acabfd1302add3db2f11e6a5478e9423a31f76660098ec0d1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121780769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44aa67983e49aa42d8b76bf170f5f607700b66a92959223601ec394e81bfb610`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 23 Jun 2022 00:59:08 GMT
ADD file:59a6186285c4849971ea2d4801e6ebc1e4310f5e3dc0f87389f39d1fa8a63c58 in / 
# Thu, 23 Jun 2022 00:59:10 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:46:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:46:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 24 Jun 2022 21:27:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 21:27:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 11 Jul 2022 23:26:39 GMT
ENV TELEGRAF_VERSION=1.23.2
# Mon, 11 Jul 2022 23:26:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 11 Jul 2022 23:26:52 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 11 Jul 2022 23:26:53 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Mon, 11 Jul 2022 23:26:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 23:26:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2147df557f50051066d8920b460727b890c1da5cb2c15b055c99ed8216b5528f`  
		Last Modified: Thu, 23 Jun 2022 01:14:34 GMT  
		Size: 50.2 MB (50199604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b28303e18c4d3b1788071e1a67ed51ad28c9574bf30371176fc152638acdbe`  
		Last Modified: Thu, 23 Jun 2022 02:13:15 GMT  
		Size: 4.9 MB (4924846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536c76bf1b84e75e4834c8b50a6f3697460303c4b2021434891103b94ca78fac`  
		Last Modified: Thu, 23 Jun 2022 02:13:17 GMT  
		Size: 10.2 MB (10217964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b88c9ed26d6ff0f4b0867529070d09c287497b1865129fafeec1cf7ef55060`  
		Last Modified: Fri, 24 Jun 2022 21:29:21 GMT  
		Size: 17.5 MB (17462442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977396ca6613b43fc974eb62e58778ddcfbb3a5035f9004822ed9790558903cc`  
		Last Modified: Fri, 24 Jun 2022 21:29:09 GMT  
		Size: 2.9 KB (2885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd936129f97b2c51f76b1dec4ab132c4d49ddf289efad281471c0a32dbb18b6`  
		Last Modified: Mon, 11 Jul 2022 23:28:15 GMT  
		Size: 39.0 MB (38972686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c962285d77bbf00d8db24ba7ddbe041d624fc73fda84df9bdeb5d6da10c17c`  
		Last Modified: Mon, 11 Jul 2022 23:27:47 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c0ff55d092c30d7ecd3e6f6e1c560e5400c5988417c3771b71ec7fce568d6dcb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125552909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027feea3fe9199ac2ea2857f4c86234cf752740055fe04a18c6a38c8d4c2de87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:28 GMT
ADD file:64c455af1bb18ff2c202a244e058b6e5ac147b89410ed36edc5e29f4b6f02c5d in / 
# Thu, 23 Jun 2022 00:40:29 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:11:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:11:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 19:55:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 19:55:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 11 Jul 2022 22:44:26 GMT
ENV TELEGRAF_VERSION=1.23.2
# Mon, 11 Jul 2022 22:44:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 11 Jul 2022 22:44:32 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 11 Jul 2022 22:44:34 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Mon, 11 Jul 2022 22:44:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:44:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f873dfbc59b181817d5bc2b9fc31d90d8f9139c8cabb2fa7264f9bd7b418b8d2`  
		Last Modified: Thu, 23 Jun 2022 00:46:51 GMT  
		Size: 53.7 MB (53696815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b65e0e9cdc28c8cedaabbc5cbae4652c9b107c47684de49f01a77741a5ded`  
		Last Modified: Thu, 23 Jun 2022 01:21:51 GMT  
		Size: 4.9 MB (4938760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43836e7983cba8b758620a218a0ee622daf5513308b6a9e8316f94c271ecafd`  
		Last Modified: Thu, 23 Jun 2022 01:21:51 GMT  
		Size: 10.7 MB (10656970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a562e1b7ad1377d92aba29b26704c595b6a1af4bc32125b2786abcc8de603d4`  
		Last Modified: Thu, 23 Jun 2022 19:56:09 GMT  
		Size: 18.4 MB (18382892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c5c3d4f7e18eed5baaf38a346806cbe4e8430ecd3604e7f627019694133f8d`  
		Last Modified: Thu, 23 Jun 2022 19:56:05 GMT  
		Size: 2.9 KB (2868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29edc08f15fffc2e2c687a005f7c294aea098cfbbec504d91ab6f4abab32cfb`  
		Last Modified: Mon, 11 Jul 2022 22:45:05 GMT  
		Size: 37.9 MB (37874260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265079157eba3d81645ac29bb2c61b9aae40d744c12e946daee29c070e072123`  
		Last Modified: Mon, 11 Jul 2022 22:44:59 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
