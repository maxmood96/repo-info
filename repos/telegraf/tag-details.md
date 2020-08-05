<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.13`](#telegraf113)
-	[`telegraf:1.13.4`](#telegraf1134)
-	[`telegraf:1.13.4-alpine`](#telegraf1134-alpine)
-	[`telegraf:1.13-alpine`](#telegraf113-alpine)
-	[`telegraf:1.14`](#telegraf114)
-	[`telegraf:1.14.5`](#telegraf1145)
-	[`telegraf:1.14.5-alpine`](#telegraf1145-alpine)
-	[`telegraf:1.14-alpine`](#telegraf114-alpine)
-	[`telegraf:1.15`](#telegraf115)
-	[`telegraf:1.15.2`](#telegraf1152)
-	[`telegraf:1.15.2-alpine`](#telegraf1152-alpine)
-	[`telegraf:1.15-alpine`](#telegraf115-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.13`

```console
$ docker pull telegraf@sha256:c6f6ae6822cde81525e826c8873827255f44949721cbca7896f49b9758dbcd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.13` - linux; amd64

```console
$ docker pull telegraf@sha256:54ceeee7ee0bb70d499702ed10123dc7e96ebf29d6646205dcbcddcd2cf15821
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96736602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e1e42ae9df5ec22a1751488eae68537c26e9b126e4a63e6a75615a541daa30`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:32 GMT
ADD file:a28d8a949b7577768d87fcbac346797fc5f7bad0539625339edcd09a32d6bf77 in / 
# Tue, 04 Aug 2020 15:45:33 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:35:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:36:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 16:36:48 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 16:36:51 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 16:36:51 GMT
ENV TELEGRAF_VERSION=1.13.4
# Wed, 05 Aug 2020 16:36:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 16:36:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 16:36:54 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 16:36:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 16:36:55 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:419e7ae5bb1e4875c367f3249b7bb7f8f39dd27dfceb4ee9d6a92191ed1c452f`  
		Last Modified: Tue, 04 Aug 2020 15:52:05 GMT  
		Size: 45.4 MB (45366706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848839e0cd3b3acc96db8a39c4520a40f98dc8f3a2a5f80b575ff4a1c88f1fcf`  
		Last Modified: Tue, 04 Aug 2020 23:42:18 GMT  
		Size: 10.8 MB (10750599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de30e8b35015c7302e071e9c2b449290f270feaf2a419f6466a555b6907e7d72`  
		Last Modified: Tue, 04 Aug 2020 23:42:17 GMT  
		Size: 4.3 MB (4339945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49bd614d49372acb0532a35c9f6740dfe07af9de936b590e0b3a96d2874317d`  
		Last Modified: Wed, 05 Aug 2020 16:37:44 GMT  
		Size: 16.0 MB (15964575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377f7d692f5db8d7ec2e76a2ae776b5fcb3058e9718c01659aa8c8d2a89e1a58`  
		Last Modified: Wed, 05 Aug 2020 16:37:40 GMT  
		Size: 2.8 KB (2775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe21b663c72cca8e6a6742a0bd35fcd3eb445f846024b4f36aad4510f3b0041`  
		Last Modified: Wed, 05 Aug 2020 16:37:45 GMT  
		Size: 20.3 MB (20311820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3618be6b620bf62118c5ec60ea39bca973e283e8fef162630f513437c10cdaee`  
		Last Modified: Wed, 05 Aug 2020 16:37:40 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.13` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:5d673989e66769a5513367d85e080fde3822d19e554b54f5b3330884e64dcb53
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89365801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f561e9757bb1d1e59cd09955462ec830b0c62d2dd2083021fa078d392888bcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:04 GMT
ADD file:0ba6f3203fb10e66124d03088d234e92fc908c572ec7eed268e866623a383a7d in / 
# Tue, 04 Aug 2020 05:01:07 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:16:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:16:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 01:50:08 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 01:50:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 01:50:17 GMT
ENV TELEGRAF_VERSION=1.13.4
# Wed, 05 Aug 2020 01:50:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 01:50:38 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 01:50:41 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 01:50:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 01:50:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:323178d00ec2c5eb5ffb9cb696a52eaf8683dcf2eb605c742da2953556f06e37`  
		Last Modified: Tue, 04 Aug 2020 05:08:40 GMT  
		Size: 42.1 MB (42111382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b4e15a79453f6ae10815d79c8f4590aef2f1ac2979c192ff7f1ed0fbf04e60`  
		Last Modified: Tue, 04 Aug 2020 08:30:43 GMT  
		Size: 9.4 MB (9443881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9cb1ef704caf3af8a2ed43dc12884b4f74ac867ce95f60bd8996f51fde770`  
		Last Modified: Tue, 04 Aug 2020 08:30:41 GMT  
		Size: 3.9 MB (3918490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31269b8e0d90f2c135d09e726df2432c9dd0c2b91d454425d5bb545df4485c9d`  
		Last Modified: Wed, 05 Aug 2020 01:53:21 GMT  
		Size: 14.8 MB (14835952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828e4df8803d59fb1a424adf9f6a9282d704a9ea887b6408ec71f58139d202cf`  
		Last Modified: Wed, 05 Aug 2020 01:53:16 GMT  
		Size: 2.8 KB (2800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760e1a5f7d40803dfa08cc45f67bf3b683066eb90166a26dba73340aee980680`  
		Last Modified: Wed, 05 Aug 2020 01:53:23 GMT  
		Size: 19.1 MB (19053114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5572699b74f4f50dd2a5039ae8a729818252806147867d6993360da0c68cf774`  
		Last Modified: Wed, 05 Aug 2020 01:53:16 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.13` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:543df9d4ddfccede8f696e3e50555dce51bd8aeaec119eb532486179273046a7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91197856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81eb40d0f039a5fd30853c08feaf870ad63befc41461cd8c184ae3199ee59434`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 06:59:38 GMT
ADD file:0a7a65de4c9dc6ea7f7ac97362a47b82a02a45ecab668ddc84cfd011dad26d33 in / 
# Tue, 04 Aug 2020 06:59:41 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:16:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:16:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 08:09:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 08:10:02 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 08:10:03 GMT
ENV TELEGRAF_VERSION=1.13.4
# Wed, 05 Aug 2020 08:10:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 08:10:09 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 08:10:09 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 08:10:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 08:10:11 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708f9b01fc1a5dff70f7d40443ac7dd0ee1d0ae93202b6f305f4e3627cea7d22`  
		Last Modified: Tue, 04 Aug 2020 07:06:12 GMT  
		Size: 43.2 MB (43171643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc3a0299d558e9f611edd56658d792af018276662c8c30d86476a05c18b00b`  
		Last Modified: Tue, 04 Aug 2020 11:26:22 GMT  
		Size: 9.7 MB (9700890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feaa2634e51f929e9ca86765cd5579cdf0809084c80d6787166627ca2aed6d4`  
		Last Modified: Tue, 04 Aug 2020 11:26:21 GMT  
		Size: 4.1 MB (4094122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09117e7e6f18755efa6d9f88ecae23e3ea6761a5710cdb85095a08a3fd4a25fd`  
		Last Modified: Wed, 05 Aug 2020 08:12:05 GMT  
		Size: 15.5 MB (15522893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ed5e8840726f09762475435173bb2d5c0de509101a8eec5862cb87b8b53e5a`  
		Last Modified: Wed, 05 Aug 2020 08:11:59 GMT  
		Size: 2.8 KB (2802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ac96ce13d32e1764ae2ec8cac422f92f755091bd2f2fac85f5947477af559`  
		Last Modified: Wed, 05 Aug 2020 08:12:06 GMT  
		Size: 18.7 MB (18705322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90866c9a7854cdb1b0b4d14db41a888c6419d1f9ca994378dbcd955cf6335c74`  
		Last Modified: Wed, 05 Aug 2020 08:12:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.13.4`

```console
$ docker pull telegraf@sha256:c6f6ae6822cde81525e826c8873827255f44949721cbca7896f49b9758dbcd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.13.4` - linux; amd64

```console
$ docker pull telegraf@sha256:54ceeee7ee0bb70d499702ed10123dc7e96ebf29d6646205dcbcddcd2cf15821
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96736602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e1e42ae9df5ec22a1751488eae68537c26e9b126e4a63e6a75615a541daa30`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:32 GMT
ADD file:a28d8a949b7577768d87fcbac346797fc5f7bad0539625339edcd09a32d6bf77 in / 
# Tue, 04 Aug 2020 15:45:33 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:35:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:36:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 16:36:48 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 16:36:51 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 16:36:51 GMT
ENV TELEGRAF_VERSION=1.13.4
# Wed, 05 Aug 2020 16:36:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 16:36:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 16:36:54 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 16:36:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 16:36:55 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:419e7ae5bb1e4875c367f3249b7bb7f8f39dd27dfceb4ee9d6a92191ed1c452f`  
		Last Modified: Tue, 04 Aug 2020 15:52:05 GMT  
		Size: 45.4 MB (45366706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848839e0cd3b3acc96db8a39c4520a40f98dc8f3a2a5f80b575ff4a1c88f1fcf`  
		Last Modified: Tue, 04 Aug 2020 23:42:18 GMT  
		Size: 10.8 MB (10750599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de30e8b35015c7302e071e9c2b449290f270feaf2a419f6466a555b6907e7d72`  
		Last Modified: Tue, 04 Aug 2020 23:42:17 GMT  
		Size: 4.3 MB (4339945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49bd614d49372acb0532a35c9f6740dfe07af9de936b590e0b3a96d2874317d`  
		Last Modified: Wed, 05 Aug 2020 16:37:44 GMT  
		Size: 16.0 MB (15964575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377f7d692f5db8d7ec2e76a2ae776b5fcb3058e9718c01659aa8c8d2a89e1a58`  
		Last Modified: Wed, 05 Aug 2020 16:37:40 GMT  
		Size: 2.8 KB (2775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe21b663c72cca8e6a6742a0bd35fcd3eb445f846024b4f36aad4510f3b0041`  
		Last Modified: Wed, 05 Aug 2020 16:37:45 GMT  
		Size: 20.3 MB (20311820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3618be6b620bf62118c5ec60ea39bca973e283e8fef162630f513437c10cdaee`  
		Last Modified: Wed, 05 Aug 2020 16:37:40 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.13.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:5d673989e66769a5513367d85e080fde3822d19e554b54f5b3330884e64dcb53
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89365801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f561e9757bb1d1e59cd09955462ec830b0c62d2dd2083021fa078d392888bcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:04 GMT
ADD file:0ba6f3203fb10e66124d03088d234e92fc908c572ec7eed268e866623a383a7d in / 
# Tue, 04 Aug 2020 05:01:07 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:16:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:16:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 01:50:08 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 01:50:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 01:50:17 GMT
ENV TELEGRAF_VERSION=1.13.4
# Wed, 05 Aug 2020 01:50:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 01:50:38 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 01:50:41 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 01:50:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 01:50:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:323178d00ec2c5eb5ffb9cb696a52eaf8683dcf2eb605c742da2953556f06e37`  
		Last Modified: Tue, 04 Aug 2020 05:08:40 GMT  
		Size: 42.1 MB (42111382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b4e15a79453f6ae10815d79c8f4590aef2f1ac2979c192ff7f1ed0fbf04e60`  
		Last Modified: Tue, 04 Aug 2020 08:30:43 GMT  
		Size: 9.4 MB (9443881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9cb1ef704caf3af8a2ed43dc12884b4f74ac867ce95f60bd8996f51fde770`  
		Last Modified: Tue, 04 Aug 2020 08:30:41 GMT  
		Size: 3.9 MB (3918490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31269b8e0d90f2c135d09e726df2432c9dd0c2b91d454425d5bb545df4485c9d`  
		Last Modified: Wed, 05 Aug 2020 01:53:21 GMT  
		Size: 14.8 MB (14835952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828e4df8803d59fb1a424adf9f6a9282d704a9ea887b6408ec71f58139d202cf`  
		Last Modified: Wed, 05 Aug 2020 01:53:16 GMT  
		Size: 2.8 KB (2800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760e1a5f7d40803dfa08cc45f67bf3b683066eb90166a26dba73340aee980680`  
		Last Modified: Wed, 05 Aug 2020 01:53:23 GMT  
		Size: 19.1 MB (19053114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5572699b74f4f50dd2a5039ae8a729818252806147867d6993360da0c68cf774`  
		Last Modified: Wed, 05 Aug 2020 01:53:16 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.13.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:543df9d4ddfccede8f696e3e50555dce51bd8aeaec119eb532486179273046a7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91197856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81eb40d0f039a5fd30853c08feaf870ad63befc41461cd8c184ae3199ee59434`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 06:59:38 GMT
ADD file:0a7a65de4c9dc6ea7f7ac97362a47b82a02a45ecab668ddc84cfd011dad26d33 in / 
# Tue, 04 Aug 2020 06:59:41 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:16:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:16:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 08:09:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 08:10:02 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 08:10:03 GMT
ENV TELEGRAF_VERSION=1.13.4
# Wed, 05 Aug 2020 08:10:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 08:10:09 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 08:10:09 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 08:10:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 08:10:11 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708f9b01fc1a5dff70f7d40443ac7dd0ee1d0ae93202b6f305f4e3627cea7d22`  
		Last Modified: Tue, 04 Aug 2020 07:06:12 GMT  
		Size: 43.2 MB (43171643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc3a0299d558e9f611edd56658d792af018276662c8c30d86476a05c18b00b`  
		Last Modified: Tue, 04 Aug 2020 11:26:22 GMT  
		Size: 9.7 MB (9700890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feaa2634e51f929e9ca86765cd5579cdf0809084c80d6787166627ca2aed6d4`  
		Last Modified: Tue, 04 Aug 2020 11:26:21 GMT  
		Size: 4.1 MB (4094122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09117e7e6f18755efa6d9f88ecae23e3ea6761a5710cdb85095a08a3fd4a25fd`  
		Last Modified: Wed, 05 Aug 2020 08:12:05 GMT  
		Size: 15.5 MB (15522893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ed5e8840726f09762475435173bb2d5c0de509101a8eec5862cb87b8b53e5a`  
		Last Modified: Wed, 05 Aug 2020 08:11:59 GMT  
		Size: 2.8 KB (2802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ac96ce13d32e1764ae2ec8cac422f92f755091bd2f2fac85f5947477af559`  
		Last Modified: Wed, 05 Aug 2020 08:12:06 GMT  
		Size: 18.7 MB (18705322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90866c9a7854cdb1b0b4d14db41a888c6419d1f9ca994378dbcd955cf6335c74`  
		Last Modified: Wed, 05 Aug 2020 08:12:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.13.4-alpine`

```console
$ docker pull telegraf@sha256:7f8f7e96dd88004235d520cafd6cbfe19e5d58774a0e898a12bab78c6b614db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.13.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:d5b369da4f66716e75be5a52479dee1df89f63fae50d7cb38b4d4c9f9b152065
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26785600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0ea837d9c4d908e723d2caa29dd9c24b186e16151a366fcafc23847073738a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:24:06 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Fri, 24 Apr 2020 14:24:18 GMT
ENV TELEGRAF_VERSION=1.13.4
# Thu, 23 Jul 2020 05:21:28 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/telegraf.conf /etc/telegraf/ &&     chmod +x /usr/src/telegraf*/* &&     cp -a /usr/src/telegraf*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jul 2020 05:21:28 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 23 Jul 2020 05:21:29 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 23 Jul 2020 05:21:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jul 2020 05:21:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21ceaab89b626cc487c744b86ea671176e8adf45ada4605d74c66278d136829`  
		Last Modified: Fri, 24 Apr 2020 14:24:49 GMT  
		Size: 3.7 MB (3720297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23772ee9e9fcd665e00d10df2027c045d162c2296df6f2ed51f5d17f5692589`  
		Last Modified: Thu, 23 Jul 2020 05:22:39 GMT  
		Size: 20.3 MB (20291554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418d83e33a75475b1f2a33ff092da859c941ac38940aed7984edaf6784ede0ea`  
		Last Modified: Thu, 23 Jul 2020 05:22:35 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.13-alpine`

```console
$ docker pull telegraf@sha256:7f8f7e96dd88004235d520cafd6cbfe19e5d58774a0e898a12bab78c6b614db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.13-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:d5b369da4f66716e75be5a52479dee1df89f63fae50d7cb38b4d4c9f9b152065
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26785600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0ea837d9c4d908e723d2caa29dd9c24b186e16151a366fcafc23847073738a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:24:06 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Fri, 24 Apr 2020 14:24:18 GMT
ENV TELEGRAF_VERSION=1.13.4
# Thu, 23 Jul 2020 05:21:28 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/telegraf.conf /etc/telegraf/ &&     chmod +x /usr/src/telegraf*/* &&     cp -a /usr/src/telegraf*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jul 2020 05:21:28 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 23 Jul 2020 05:21:29 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 23 Jul 2020 05:21:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jul 2020 05:21:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21ceaab89b626cc487c744b86ea671176e8adf45ada4605d74c66278d136829`  
		Last Modified: Fri, 24 Apr 2020 14:24:49 GMT  
		Size: 3.7 MB (3720297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23772ee9e9fcd665e00d10df2027c045d162c2296df6f2ed51f5d17f5692589`  
		Last Modified: Thu, 23 Jul 2020 05:22:39 GMT  
		Size: 20.3 MB (20291554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418d83e33a75475b1f2a33ff092da859c941ac38940aed7984edaf6784ede0ea`  
		Last Modified: Thu, 23 Jul 2020 05:22:35 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.14`

```console
$ docker pull telegraf@sha256:81d74fa7f2357236eaf73f09e47d4a7992d0b4ed4031734a618a39b306b2e8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.14` - linux; amd64

```console
$ docker pull telegraf@sha256:1e9ebcb9b3ee622619696e97ffac059af54e65fbf06fe709acce88b04d272c9d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97842151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39fa26a650c970c2ed06da9f4e4ba2c8d40f12e22e56e00ff6d72cc12c2001af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:32 GMT
ADD file:a28d8a949b7577768d87fcbac346797fc5f7bad0539625339edcd09a32d6bf77 in / 
# Tue, 04 Aug 2020 15:45:33 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:35:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:36:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 16:36:48 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 16:36:51 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 16:37:04 GMT
ENV TELEGRAF_VERSION=1.14.5
# Wed, 05 Aug 2020 16:37:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 16:37:06 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 16:37:06 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 16:37:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 16:37:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:419e7ae5bb1e4875c367f3249b7bb7f8f39dd27dfceb4ee9d6a92191ed1c452f`  
		Last Modified: Tue, 04 Aug 2020 15:52:05 GMT  
		Size: 45.4 MB (45366706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848839e0cd3b3acc96db8a39c4520a40f98dc8f3a2a5f80b575ff4a1c88f1fcf`  
		Last Modified: Tue, 04 Aug 2020 23:42:18 GMT  
		Size: 10.8 MB (10750599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de30e8b35015c7302e071e9c2b449290f270feaf2a419f6466a555b6907e7d72`  
		Last Modified: Tue, 04 Aug 2020 23:42:17 GMT  
		Size: 4.3 MB (4339945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49bd614d49372acb0532a35c9f6740dfe07af9de936b590e0b3a96d2874317d`  
		Last Modified: Wed, 05 Aug 2020 16:37:44 GMT  
		Size: 16.0 MB (15964575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377f7d692f5db8d7ec2e76a2ae776b5fcb3058e9718c01659aa8c8d2a89e1a58`  
		Last Modified: Wed, 05 Aug 2020 16:37:40 GMT  
		Size: 2.8 KB (2775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3861b69397f0ed00ada120f2b24848a1ef6ae22efc80f0963fa27fec55768ab9`  
		Last Modified: Wed, 05 Aug 2020 16:37:54 GMT  
		Size: 21.4 MB (21417368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1203470c4c7b920b1fbe49e9d3da408129872c4eebd2ffc60eee73ab9a636644`  
		Last Modified: Wed, 05 Aug 2020 16:37:50 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.14` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8830801f1a26eda4113d15f4525d1a8f129ccc32d3a3b449d9840fec03528b83
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.4 MB (90442981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a17d7e9820b6b4020850fcebff2bc885b1eeaebac6b85089fdc812f4df2f23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:04 GMT
ADD file:0ba6f3203fb10e66124d03088d234e92fc908c572ec7eed268e866623a383a7d in / 
# Tue, 04 Aug 2020 05:01:07 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:16:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:16:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 01:50:08 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 01:50:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 01:51:00 GMT
ENV TELEGRAF_VERSION=1.14.5
# Wed, 05 Aug 2020 01:51:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 01:51:15 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 01:51:20 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 01:51:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 01:51:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:323178d00ec2c5eb5ffb9cb696a52eaf8683dcf2eb605c742da2953556f06e37`  
		Last Modified: Tue, 04 Aug 2020 05:08:40 GMT  
		Size: 42.1 MB (42111382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b4e15a79453f6ae10815d79c8f4590aef2f1ac2979c192ff7f1ed0fbf04e60`  
		Last Modified: Tue, 04 Aug 2020 08:30:43 GMT  
		Size: 9.4 MB (9443881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9cb1ef704caf3af8a2ed43dc12884b4f74ac867ce95f60bd8996f51fde770`  
		Last Modified: Tue, 04 Aug 2020 08:30:41 GMT  
		Size: 3.9 MB (3918490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31269b8e0d90f2c135d09e726df2432c9dd0c2b91d454425d5bb545df4485c9d`  
		Last Modified: Wed, 05 Aug 2020 01:53:21 GMT  
		Size: 14.8 MB (14835952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828e4df8803d59fb1a424adf9f6a9282d704a9ea887b6408ec71f58139d202cf`  
		Last Modified: Wed, 05 Aug 2020 01:53:16 GMT  
		Size: 2.8 KB (2800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd152d9628a7fff5603b5b86e79c2d8c3cdacbb165a79181cae693402e8005f4`  
		Last Modified: Wed, 05 Aug 2020 01:53:37 GMT  
		Size: 20.1 MB (20130294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbeee2190b708757e9239b378f9ba74d39d498a3dfa58bd2b874d9cc9824347`  
		Last Modified: Wed, 05 Aug 2020 01:53:29 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.14` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:fcdeadf968cb8edd513868ffe9b52152dfc0c7f76a8719d0c259bcfce4913403
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92214166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8667b45b68c6ab7d1d04c863c811fab83c3e93a2b658797f47fb705361be03b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 06:59:38 GMT
ADD file:0a7a65de4c9dc6ea7f7ac97362a47b82a02a45ecab668ddc84cfd011dad26d33 in / 
# Tue, 04 Aug 2020 06:59:41 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:16:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:16:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 08:09:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 08:10:02 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 08:10:20 GMT
ENV TELEGRAF_VERSION=1.14.5
# Wed, 05 Aug 2020 08:10:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 08:10:27 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 08:10:28 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 08:10:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 08:10:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708f9b01fc1a5dff70f7d40443ac7dd0ee1d0ae93202b6f305f4e3627cea7d22`  
		Last Modified: Tue, 04 Aug 2020 07:06:12 GMT  
		Size: 43.2 MB (43171643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc3a0299d558e9f611edd56658d792af018276662c8c30d86476a05c18b00b`  
		Last Modified: Tue, 04 Aug 2020 11:26:22 GMT  
		Size: 9.7 MB (9700890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feaa2634e51f929e9ca86765cd5579cdf0809084c80d6787166627ca2aed6d4`  
		Last Modified: Tue, 04 Aug 2020 11:26:21 GMT  
		Size: 4.1 MB (4094122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09117e7e6f18755efa6d9f88ecae23e3ea6761a5710cdb85095a08a3fd4a25fd`  
		Last Modified: Wed, 05 Aug 2020 08:12:05 GMT  
		Size: 15.5 MB (15522893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ed5e8840726f09762475435173bb2d5c0de509101a8eec5862cb87b8b53e5a`  
		Last Modified: Wed, 05 Aug 2020 08:11:59 GMT  
		Size: 2.8 KB (2802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d425e4df7cd5de0a73524f6fce8cf80fc0019e50dc593277ab002e1276d3b85`  
		Last Modified: Wed, 05 Aug 2020 08:12:19 GMT  
		Size: 19.7 MB (19721630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e904a0f0de968ed72852c65573643d8345d4eb9edab91524a722b16331dbc`  
		Last Modified: Wed, 05 Aug 2020 08:12:12 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.14.5`

```console
$ docker pull telegraf@sha256:81d74fa7f2357236eaf73f09e47d4a7992d0b4ed4031734a618a39b306b2e8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.14.5` - linux; amd64

```console
$ docker pull telegraf@sha256:1e9ebcb9b3ee622619696e97ffac059af54e65fbf06fe709acce88b04d272c9d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97842151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39fa26a650c970c2ed06da9f4e4ba2c8d40f12e22e56e00ff6d72cc12c2001af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:32 GMT
ADD file:a28d8a949b7577768d87fcbac346797fc5f7bad0539625339edcd09a32d6bf77 in / 
# Tue, 04 Aug 2020 15:45:33 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:35:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:36:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 16:36:48 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 16:36:51 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 16:37:04 GMT
ENV TELEGRAF_VERSION=1.14.5
# Wed, 05 Aug 2020 16:37:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 16:37:06 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 16:37:06 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 16:37:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 16:37:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:419e7ae5bb1e4875c367f3249b7bb7f8f39dd27dfceb4ee9d6a92191ed1c452f`  
		Last Modified: Tue, 04 Aug 2020 15:52:05 GMT  
		Size: 45.4 MB (45366706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848839e0cd3b3acc96db8a39c4520a40f98dc8f3a2a5f80b575ff4a1c88f1fcf`  
		Last Modified: Tue, 04 Aug 2020 23:42:18 GMT  
		Size: 10.8 MB (10750599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de30e8b35015c7302e071e9c2b449290f270feaf2a419f6466a555b6907e7d72`  
		Last Modified: Tue, 04 Aug 2020 23:42:17 GMT  
		Size: 4.3 MB (4339945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49bd614d49372acb0532a35c9f6740dfe07af9de936b590e0b3a96d2874317d`  
		Last Modified: Wed, 05 Aug 2020 16:37:44 GMT  
		Size: 16.0 MB (15964575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377f7d692f5db8d7ec2e76a2ae776b5fcb3058e9718c01659aa8c8d2a89e1a58`  
		Last Modified: Wed, 05 Aug 2020 16:37:40 GMT  
		Size: 2.8 KB (2775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3861b69397f0ed00ada120f2b24848a1ef6ae22efc80f0963fa27fec55768ab9`  
		Last Modified: Wed, 05 Aug 2020 16:37:54 GMT  
		Size: 21.4 MB (21417368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1203470c4c7b920b1fbe49e9d3da408129872c4eebd2ffc60eee73ab9a636644`  
		Last Modified: Wed, 05 Aug 2020 16:37:50 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.14.5` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8830801f1a26eda4113d15f4525d1a8f129ccc32d3a3b449d9840fec03528b83
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.4 MB (90442981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a17d7e9820b6b4020850fcebff2bc885b1eeaebac6b85089fdc812f4df2f23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:04 GMT
ADD file:0ba6f3203fb10e66124d03088d234e92fc908c572ec7eed268e866623a383a7d in / 
# Tue, 04 Aug 2020 05:01:07 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:16:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:16:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 01:50:08 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 01:50:16 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 01:51:00 GMT
ENV TELEGRAF_VERSION=1.14.5
# Wed, 05 Aug 2020 01:51:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 01:51:15 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 01:51:20 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 01:51:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 01:51:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:323178d00ec2c5eb5ffb9cb696a52eaf8683dcf2eb605c742da2953556f06e37`  
		Last Modified: Tue, 04 Aug 2020 05:08:40 GMT  
		Size: 42.1 MB (42111382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b4e15a79453f6ae10815d79c8f4590aef2f1ac2979c192ff7f1ed0fbf04e60`  
		Last Modified: Tue, 04 Aug 2020 08:30:43 GMT  
		Size: 9.4 MB (9443881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9cb1ef704caf3af8a2ed43dc12884b4f74ac867ce95f60bd8996f51fde770`  
		Last Modified: Tue, 04 Aug 2020 08:30:41 GMT  
		Size: 3.9 MB (3918490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31269b8e0d90f2c135d09e726df2432c9dd0c2b91d454425d5bb545df4485c9d`  
		Last Modified: Wed, 05 Aug 2020 01:53:21 GMT  
		Size: 14.8 MB (14835952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828e4df8803d59fb1a424adf9f6a9282d704a9ea887b6408ec71f58139d202cf`  
		Last Modified: Wed, 05 Aug 2020 01:53:16 GMT  
		Size: 2.8 KB (2800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd152d9628a7fff5603b5b86e79c2d8c3cdacbb165a79181cae693402e8005f4`  
		Last Modified: Wed, 05 Aug 2020 01:53:37 GMT  
		Size: 20.1 MB (20130294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbeee2190b708757e9239b378f9ba74d39d498a3dfa58bd2b874d9cc9824347`  
		Last Modified: Wed, 05 Aug 2020 01:53:29 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.14.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:fcdeadf968cb8edd513868ffe9b52152dfc0c7f76a8719d0c259bcfce4913403
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92214166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8667b45b68c6ab7d1d04c863c811fab83c3e93a2b658797f47fb705361be03b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 06:59:38 GMT
ADD file:0a7a65de4c9dc6ea7f7ac97362a47b82a02a45ecab668ddc84cfd011dad26d33 in / 
# Tue, 04 Aug 2020 06:59:41 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:16:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:16:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 08:09:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 08:10:02 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 08:10:20 GMT
ENV TELEGRAF_VERSION=1.14.5
# Wed, 05 Aug 2020 08:10:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 08:10:27 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 08:10:28 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 08:10:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 08:10:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:708f9b01fc1a5dff70f7d40443ac7dd0ee1d0ae93202b6f305f4e3627cea7d22`  
		Last Modified: Tue, 04 Aug 2020 07:06:12 GMT  
		Size: 43.2 MB (43171643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc3a0299d558e9f611edd56658d792af018276662c8c30d86476a05c18b00b`  
		Last Modified: Tue, 04 Aug 2020 11:26:22 GMT  
		Size: 9.7 MB (9700890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feaa2634e51f929e9ca86765cd5579cdf0809084c80d6787166627ca2aed6d4`  
		Last Modified: Tue, 04 Aug 2020 11:26:21 GMT  
		Size: 4.1 MB (4094122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09117e7e6f18755efa6d9f88ecae23e3ea6761a5710cdb85095a08a3fd4a25fd`  
		Last Modified: Wed, 05 Aug 2020 08:12:05 GMT  
		Size: 15.5 MB (15522893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ed5e8840726f09762475435173bb2d5c0de509101a8eec5862cb87b8b53e5a`  
		Last Modified: Wed, 05 Aug 2020 08:11:59 GMT  
		Size: 2.8 KB (2802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d425e4df7cd5de0a73524f6fce8cf80fc0019e50dc593277ab002e1276d3b85`  
		Last Modified: Wed, 05 Aug 2020 08:12:19 GMT  
		Size: 19.7 MB (19721630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e904a0f0de968ed72852c65573643d8345d4eb9edab91524a722b16331dbc`  
		Last Modified: Wed, 05 Aug 2020 08:12:12 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.14.5-alpine`

```console
$ docker pull telegraf@sha256:be834c519c2fdf3091b6f6b761a0af2ab65d1b1380a9249121e6d1d4cd3e6620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.14.5-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b3b44ebf375d984b24604a0bf423a4c566448dfc3c3690659f194c5ed1744339
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27908281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ea57f77b71e81eced3ee46d7360fc73b566f0d0f019acb1327db61cc90e4c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:24:06 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Tue, 30 Jun 2020 22:40:28 GMT
ENV TELEGRAF_VERSION=1.14.5
# Thu, 23 Jul 2020 05:21:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/telegraf.conf /etc/telegraf/ &&     chmod +x /usr/src/telegraf*/* &&     cp -a /usr/src/telegraf*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jul 2020 05:21:45 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 23 Jul 2020 05:21:46 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 23 Jul 2020 05:21:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jul 2020 05:21:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21ceaab89b626cc487c744b86ea671176e8adf45ada4605d74c66278d136829`  
		Last Modified: Fri, 24 Apr 2020 14:24:49 GMT  
		Size: 3.7 MB (3720297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938d1fac0acfc4f46464b79d3d85d9c2bbe730f0b8f99b06c9917df62a262f7`  
		Last Modified: Thu, 23 Jul 2020 05:22:55 GMT  
		Size: 21.4 MB (21414234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86782e257422d8308fa39159fe04133d0f4db9d37be5a4c984a306886bedbd8a`  
		Last Modified: Thu, 23 Jul 2020 05:22:51 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.14-alpine`

```console
$ docker pull telegraf@sha256:be834c519c2fdf3091b6f6b761a0af2ab65d1b1380a9249121e6d1d4cd3e6620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.14-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b3b44ebf375d984b24604a0bf423a4c566448dfc3c3690659f194c5ed1744339
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27908281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ea57f77b71e81eced3ee46d7360fc73b566f0d0f019acb1327db61cc90e4c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:24:06 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Tue, 30 Jun 2020 22:40:28 GMT
ENV TELEGRAF_VERSION=1.14.5
# Thu, 23 Jul 2020 05:21:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/telegraf.conf /etc/telegraf/ &&     chmod +x /usr/src/telegraf*/* &&     cp -a /usr/src/telegraf*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jul 2020 05:21:45 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 23 Jul 2020 05:21:46 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Thu, 23 Jul 2020 05:21:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jul 2020 05:21:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21ceaab89b626cc487c744b86ea671176e8adf45ada4605d74c66278d136829`  
		Last Modified: Fri, 24 Apr 2020 14:24:49 GMT  
		Size: 3.7 MB (3720297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8938d1fac0acfc4f46464b79d3d85d9c2bbe730f0b8f99b06c9917df62a262f7`  
		Last Modified: Thu, 23 Jul 2020 05:22:55 GMT  
		Size: 21.4 MB (21414234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86782e257422d8308fa39159fe04133d0f4db9d37be5a4c984a306886bedbd8a`  
		Last Modified: Thu, 23 Jul 2020 05:22:51 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.15`

```console
$ docker pull telegraf@sha256:1c5e26aa0cab13461bf8aa1b151c0095abaeff55723acf5d735ab295b942fc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.15` - linux; amd64

```console
$ docker pull telegraf@sha256:4e9dd906fb2111ba80ecf7cde0c9a624f759c410f720d141d3a9655cb4d44b61
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107281814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79fd1e5d0a8f8e6ab2ff7286476d2b2f7a06e62b13775c4af8a1606295e2a5eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:33 GMT
ADD file:4b03b5f551e3fbdf47ec609712007327828f7530cc3455c43bbcdcaf449a75a9 in / 
# Tue, 04 Aug 2020 15:42:34 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:26:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:26:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 16:37:22 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 16:37:23 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 16:37:23 GMT
ENV TELEGRAF_VERSION=1.15.2
# Wed, 05 Aug 2020 16:37:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 16:37:25 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 16:37:26 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 16:37:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 16:37:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d6ff36c9ec4822c9ff8953560f7ba41653b348a9c1136755e653575f58fbded7`  
		Last Modified: Tue, 04 Aug 2020 15:48:55 GMT  
		Size: 50.4 MB (50396000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c958d65b3090aefea91284d018b2a86530a3c8174b72616c4e76993c696a5797`  
		Last Modified: Tue, 04 Aug 2020 23:39:28 GMT  
		Size: 7.8 MB (7811570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf0a6b092f5673ec05b40edb606ce58881b2f40494251117d31805225ef064`  
		Last Modified: Tue, 04 Aug 2020 23:39:27 GMT  
		Size: 10.0 MB (9996337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a3fbe69a541e8f65ae36b041a735d62c880a81575dbbff044c5c3fc0270c92`  
		Last Modified: Wed, 05 Aug 2020 16:38:02 GMT  
		Size: 17.4 MB (17409702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a58db64865c3a91a996e3bcac7e22ba9fb1e2f1e17f972229014314b823e77a`  
		Last Modified: Wed, 05 Aug 2020 16:37:58 GMT  
		Size: 2.8 KB (2820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d707aad8b7522509ed41150ec4346ed9757dd7b9ce23404bc8001c695c119ed`  
		Last Modified: Wed, 05 Aug 2020 16:38:04 GMT  
		Size: 21.7 MB (21665200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d43c06bab41756c280d0946332594f0835249b5879a2ca787fe5062fa8ebc02`  
		Last Modified: Wed, 05 Aug 2020 16:37:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.15` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:36f6d826e9bdfbb3eccba107c6fc15736687a229abf444979acda578cccc5eeb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98881250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ee1919fa55cc5935a28896f3767fab9527815930c9c6f77cc21140f088c922`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 04:56:26 GMT
ADD file:aaf5c6340b3d662631775fa4536c2e48e9f68b6cc8d53e18fb8fd76ae41b305e in / 
# Tue, 04 Aug 2020 04:56:28 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 07:52:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 07:53:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 01:52:11 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 01:52:17 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 01:52:18 GMT
ENV TELEGRAF_VERSION=1.15.2
# Wed, 05 Aug 2020 01:52:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 01:52:28 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 01:52:29 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 01:52:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 01:52:34 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e7cf402ee4b1ba67e92813d50297a082bbdbdd4d47f6aeb62f2316b81d5dc843`  
		Last Modified: Tue, 04 Aug 2020 05:04:56 GMT  
		Size: 45.9 MB (45869261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff6bd4a89fc21d80ca6924320f86708f35ddea71c7aa34a408a5b64257c764e`  
		Last Modified: Tue, 04 Aug 2020 08:25:56 GMT  
		Size: 7.1 MB (7097820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48f5852a753b7731e5d374567ae9b64e309805758f336c76d5f13bb67c94e20`  
		Last Modified: Tue, 04 Aug 2020 08:25:56 GMT  
		Size: 9.3 MB (9343353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3640f9f6e2a57392770dada759969ada76ad0acba79f078302ef3a69700ea37e`  
		Last Modified: Wed, 05 Aug 2020 01:53:50 GMT  
		Size: 16.2 MB (16164767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450459590b912a0d6ee32ffe8ec59f466a4aa6d4971e2076e9c7a986d8990d2e`  
		Last Modified: Wed, 05 Aug 2020 01:53:44 GMT  
		Size: 2.8 KB (2848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573fa0f49a25bf49631c97a439fa4ab576aac8b682d38c2bf6af36bd61402c89`  
		Last Modified: Wed, 05 Aug 2020 01:53:50 GMT  
		Size: 20.4 MB (20403016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6192a8cf2cd051a9b61ba2206e992aa27d10653c53bc8b11fb1acf8afa473ee8`  
		Last Modified: Wed, 05 Aug 2020 01:53:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.15` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:01a37222da1e9a7bc94281bd479c3fbc5836b77eb0d87555e38b88ae4ed44465
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104132549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659ccc87d400174d5cdd5ff92f940e269ffc8e15f3241846f2a555fc838519ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 06:57:06 GMT
ADD file:ce999027b153d392f8a0f85e2e7a17b9279f3cf7ad0e45192378d527275f99c6 in / 
# Tue, 04 Aug 2020 06:57:08 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:10:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:10:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 08:11:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 08:11:34 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 08:11:34 GMT
ENV TELEGRAF_VERSION=1.15.2
# Wed, 05 Aug 2020 08:11:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 08:11:42 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 08:11:43 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 08:11:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 08:11:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d5517ee72007172d5b814636405254dea459120ce08f85777bb287d106a6a240`  
		Last Modified: Tue, 04 Aug 2020 07:03:41 GMT  
		Size: 49.2 MB (49175491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283897ad4463628bd259e1cbb5eb788e7df554b42ae17fc6f5d02c4a56035c2`  
		Last Modified: Tue, 04 Aug 2020 11:23:01 GMT  
		Size: 7.7 MB (7681458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3feb40d9f5fecfa098b8f7ece6c287c6fd61b114043c8b4647359120a7d943a3`  
		Last Modified: Tue, 04 Aug 2020 11:23:02 GMT  
		Size: 10.0 MB (9983917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de25b7c9c4b90ae60cb3bf5d21d5cdda40e683278598f2223e94766b9333c2f`  
		Last Modified: Wed, 05 Aug 2020 08:12:33 GMT  
		Size: 17.3 MB (17270209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482953fc118c18769e9d7a2d3513556d40569fff4794e1bcbd845c2bd9f77c21`  
		Last Modified: Wed, 05 Aug 2020 08:12:27 GMT  
		Size: 2.8 KB (2847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bb152b6321b05c80bbccfc9098925997ce73488af052b97cc43bcb2a9ac5a1`  
		Last Modified: Wed, 05 Aug 2020 08:12:34 GMT  
		Size: 20.0 MB (20018441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c689c05367c12d93d51f002d9b053e4e1b9dcad97b137d4901d18c56599a810`  
		Last Modified: Wed, 05 Aug 2020 08:12:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.15.2`

```console
$ docker pull telegraf@sha256:1c5e26aa0cab13461bf8aa1b151c0095abaeff55723acf5d735ab295b942fc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.15.2` - linux; amd64

```console
$ docker pull telegraf@sha256:4e9dd906fb2111ba80ecf7cde0c9a624f759c410f720d141d3a9655cb4d44b61
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107281814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79fd1e5d0a8f8e6ab2ff7286476d2b2f7a06e62b13775c4af8a1606295e2a5eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:33 GMT
ADD file:4b03b5f551e3fbdf47ec609712007327828f7530cc3455c43bbcdcaf449a75a9 in / 
# Tue, 04 Aug 2020 15:42:34 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:26:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:26:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 16:37:22 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 16:37:23 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 16:37:23 GMT
ENV TELEGRAF_VERSION=1.15.2
# Wed, 05 Aug 2020 16:37:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 16:37:25 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 16:37:26 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 16:37:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 16:37:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d6ff36c9ec4822c9ff8953560f7ba41653b348a9c1136755e653575f58fbded7`  
		Last Modified: Tue, 04 Aug 2020 15:48:55 GMT  
		Size: 50.4 MB (50396000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c958d65b3090aefea91284d018b2a86530a3c8174b72616c4e76993c696a5797`  
		Last Modified: Tue, 04 Aug 2020 23:39:28 GMT  
		Size: 7.8 MB (7811570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf0a6b092f5673ec05b40edb606ce58881b2f40494251117d31805225ef064`  
		Last Modified: Tue, 04 Aug 2020 23:39:27 GMT  
		Size: 10.0 MB (9996337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a3fbe69a541e8f65ae36b041a735d62c880a81575dbbff044c5c3fc0270c92`  
		Last Modified: Wed, 05 Aug 2020 16:38:02 GMT  
		Size: 17.4 MB (17409702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a58db64865c3a91a996e3bcac7e22ba9fb1e2f1e17f972229014314b823e77a`  
		Last Modified: Wed, 05 Aug 2020 16:37:58 GMT  
		Size: 2.8 KB (2820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d707aad8b7522509ed41150ec4346ed9757dd7b9ce23404bc8001c695c119ed`  
		Last Modified: Wed, 05 Aug 2020 16:38:04 GMT  
		Size: 21.7 MB (21665200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d43c06bab41756c280d0946332594f0835249b5879a2ca787fe5062fa8ebc02`  
		Last Modified: Wed, 05 Aug 2020 16:37:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.15.2` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:36f6d826e9bdfbb3eccba107c6fc15736687a229abf444979acda578cccc5eeb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98881250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ee1919fa55cc5935a28896f3767fab9527815930c9c6f77cc21140f088c922`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 04:56:26 GMT
ADD file:aaf5c6340b3d662631775fa4536c2e48e9f68b6cc8d53e18fb8fd76ae41b305e in / 
# Tue, 04 Aug 2020 04:56:28 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 07:52:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 07:53:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 01:52:11 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 01:52:17 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 01:52:18 GMT
ENV TELEGRAF_VERSION=1.15.2
# Wed, 05 Aug 2020 01:52:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 01:52:28 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 01:52:29 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 01:52:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 01:52:34 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e7cf402ee4b1ba67e92813d50297a082bbdbdd4d47f6aeb62f2316b81d5dc843`  
		Last Modified: Tue, 04 Aug 2020 05:04:56 GMT  
		Size: 45.9 MB (45869261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff6bd4a89fc21d80ca6924320f86708f35ddea71c7aa34a408a5b64257c764e`  
		Last Modified: Tue, 04 Aug 2020 08:25:56 GMT  
		Size: 7.1 MB (7097820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48f5852a753b7731e5d374567ae9b64e309805758f336c76d5f13bb67c94e20`  
		Last Modified: Tue, 04 Aug 2020 08:25:56 GMT  
		Size: 9.3 MB (9343353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3640f9f6e2a57392770dada759969ada76ad0acba79f078302ef3a69700ea37e`  
		Last Modified: Wed, 05 Aug 2020 01:53:50 GMT  
		Size: 16.2 MB (16164767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450459590b912a0d6ee32ffe8ec59f466a4aa6d4971e2076e9c7a986d8990d2e`  
		Last Modified: Wed, 05 Aug 2020 01:53:44 GMT  
		Size: 2.8 KB (2848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573fa0f49a25bf49631c97a439fa4ab576aac8b682d38c2bf6af36bd61402c89`  
		Last Modified: Wed, 05 Aug 2020 01:53:50 GMT  
		Size: 20.4 MB (20403016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6192a8cf2cd051a9b61ba2206e992aa27d10653c53bc8b11fb1acf8afa473ee8`  
		Last Modified: Wed, 05 Aug 2020 01:53:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.15.2` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:01a37222da1e9a7bc94281bd479c3fbc5836b77eb0d87555e38b88ae4ed44465
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104132549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659ccc87d400174d5cdd5ff92f940e269ffc8e15f3241846f2a555fc838519ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 06:57:06 GMT
ADD file:ce999027b153d392f8a0f85e2e7a17b9279f3cf7ad0e45192378d527275f99c6 in / 
# Tue, 04 Aug 2020 06:57:08 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:10:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:10:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 08:11:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 08:11:34 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 08:11:34 GMT
ENV TELEGRAF_VERSION=1.15.2
# Wed, 05 Aug 2020 08:11:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 08:11:42 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 08:11:43 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 08:11:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 08:11:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d5517ee72007172d5b814636405254dea459120ce08f85777bb287d106a6a240`  
		Last Modified: Tue, 04 Aug 2020 07:03:41 GMT  
		Size: 49.2 MB (49175491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283897ad4463628bd259e1cbb5eb788e7df554b42ae17fc6f5d02c4a56035c2`  
		Last Modified: Tue, 04 Aug 2020 11:23:01 GMT  
		Size: 7.7 MB (7681458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3feb40d9f5fecfa098b8f7ece6c287c6fd61b114043c8b4647359120a7d943a3`  
		Last Modified: Tue, 04 Aug 2020 11:23:02 GMT  
		Size: 10.0 MB (9983917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de25b7c9c4b90ae60cb3bf5d21d5cdda40e683278598f2223e94766b9333c2f`  
		Last Modified: Wed, 05 Aug 2020 08:12:33 GMT  
		Size: 17.3 MB (17270209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482953fc118c18769e9d7a2d3513556d40569fff4794e1bcbd845c2bd9f77c21`  
		Last Modified: Wed, 05 Aug 2020 08:12:27 GMT  
		Size: 2.8 KB (2847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bb152b6321b05c80bbccfc9098925997ce73488af052b97cc43bcb2a9ac5a1`  
		Last Modified: Wed, 05 Aug 2020 08:12:34 GMT  
		Size: 20.0 MB (20018441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c689c05367c12d93d51f002d9b053e4e1b9dcad97b137d4901d18c56599a810`  
		Last Modified: Wed, 05 Aug 2020 08:12:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.15.2-alpine`

```console
$ docker pull telegraf@sha256:4588b9e64c2b5b19529330f83039c0bf847e56965e7be97fe079a152b1ab1191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.15.2-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:2088425399f413db5aab554b77a0009495dd4b025f074a647f5f787254716bec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27630336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cb9c272d511903ff1ede78263c4ac5683216915d77097390edf03f5f4159e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jul 2020 05:22:11 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Tue, 04 Aug 2020 15:40:34 GMT
ENV TELEGRAF_VERSION=1.15.2
# Tue, 04 Aug 2020 15:40:38 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 04 Aug 2020 15:40:38 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 04 Aug 2020 15:40:38 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Tue, 04 Aug 2020 15:40:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Aug 2020 15:40:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3547f42c651166f2251a4fa9f58707079f419581ee31b6183fd7a3ccf47e20`  
		Last Modified: Thu, 23 Jul 2020 05:23:09 GMT  
		Size: 3.3 MB (3297119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9caf4959bf343cdda65a46cd9cb43aa1ccc11d4b3fd6556964b735da46a4dea`  
		Last Modified: Tue, 04 Aug 2020 15:41:07 GMT  
		Size: 21.5 MB (21535340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ec6efcc0fbe3b1f56468353bbad8c10aa81821b935ffc61a2bbd0f17d351cc`  
		Last Modified: Tue, 04 Aug 2020 15:41:02 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.15-alpine`

```console
$ docker pull telegraf@sha256:4588b9e64c2b5b19529330f83039c0bf847e56965e7be97fe079a152b1ab1191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:1.15-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:2088425399f413db5aab554b77a0009495dd4b025f074a647f5f787254716bec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27630336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cb9c272d511903ff1ede78263c4ac5683216915d77097390edf03f5f4159e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jul 2020 05:22:11 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Tue, 04 Aug 2020 15:40:34 GMT
ENV TELEGRAF_VERSION=1.15.2
# Tue, 04 Aug 2020 15:40:38 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 04 Aug 2020 15:40:38 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 04 Aug 2020 15:40:38 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Tue, 04 Aug 2020 15:40:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Aug 2020 15:40:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3547f42c651166f2251a4fa9f58707079f419581ee31b6183fd7a3ccf47e20`  
		Last Modified: Thu, 23 Jul 2020 05:23:09 GMT  
		Size: 3.3 MB (3297119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9caf4959bf343cdda65a46cd9cb43aa1ccc11d4b3fd6556964b735da46a4dea`  
		Last Modified: Tue, 04 Aug 2020 15:41:07 GMT  
		Size: 21.5 MB (21535340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ec6efcc0fbe3b1f56468353bbad8c10aa81821b935ffc61a2bbd0f17d351cc`  
		Last Modified: Tue, 04 Aug 2020 15:41:02 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:4588b9e64c2b5b19529330f83039c0bf847e56965e7be97fe079a152b1ab1191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:2088425399f413db5aab554b77a0009495dd4b025f074a647f5f787254716bec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27630336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cb9c272d511903ff1ede78263c4ac5683216915d77097390edf03f5f4159e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 23 Jul 2020 05:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jul 2020 05:22:11 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata &&     update-ca-certificates
# Tue, 04 Aug 2020 15:40:34 GMT
ENV TELEGRAF_VERSION=1.15.2
# Tue, 04 Aug 2020 15:40:38 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 04 Aug 2020 15:40:38 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 04 Aug 2020 15:40:38 GMT
COPY file:a8a66b0d8dac2aee66897c63ce9b7a3d282bb5d7b796ffb12c2cd9227fed341b in /entrypoint.sh 
# Tue, 04 Aug 2020 15:40:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Aug 2020 15:40:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ed77ee1a57b06efa2aeb4cc06845d93ce8c6e8b2ca507267000b5a6edddffa`  
		Last Modified: Thu, 23 Jul 2020 05:23:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3547f42c651166f2251a4fa9f58707079f419581ee31b6183fd7a3ccf47e20`  
		Last Modified: Thu, 23 Jul 2020 05:23:09 GMT  
		Size: 3.3 MB (3297119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9caf4959bf343cdda65a46cd9cb43aa1ccc11d4b3fd6556964b735da46a4dea`  
		Last Modified: Tue, 04 Aug 2020 15:41:07 GMT  
		Size: 21.5 MB (21535340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ec6efcc0fbe3b1f56468353bbad8c10aa81821b935ffc61a2bbd0f17d351cc`  
		Last Modified: Tue, 04 Aug 2020 15:41:02 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:1c5e26aa0cab13461bf8aa1b151c0095abaeff55723acf5d735ab295b942fc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:4e9dd906fb2111ba80ecf7cde0c9a624f759c410f720d141d3a9655cb4d44b61
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107281814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79fd1e5d0a8f8e6ab2ff7286476d2b2f7a06e62b13775c4af8a1606295e2a5eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:33 GMT
ADD file:4b03b5f551e3fbdf47ec609712007327828f7530cc3455c43bbcdcaf449a75a9 in / 
# Tue, 04 Aug 2020 15:42:34 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:26:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:26:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 16:37:22 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 16:37:23 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 16:37:23 GMT
ENV TELEGRAF_VERSION=1.15.2
# Wed, 05 Aug 2020 16:37:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 16:37:25 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 16:37:26 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 16:37:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 16:37:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d6ff36c9ec4822c9ff8953560f7ba41653b348a9c1136755e653575f58fbded7`  
		Last Modified: Tue, 04 Aug 2020 15:48:55 GMT  
		Size: 50.4 MB (50396000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c958d65b3090aefea91284d018b2a86530a3c8174b72616c4e76993c696a5797`  
		Last Modified: Tue, 04 Aug 2020 23:39:28 GMT  
		Size: 7.8 MB (7811570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf0a6b092f5673ec05b40edb606ce58881b2f40494251117d31805225ef064`  
		Last Modified: Tue, 04 Aug 2020 23:39:27 GMT  
		Size: 10.0 MB (9996337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a3fbe69a541e8f65ae36b041a735d62c880a81575dbbff044c5c3fc0270c92`  
		Last Modified: Wed, 05 Aug 2020 16:38:02 GMT  
		Size: 17.4 MB (17409702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a58db64865c3a91a996e3bcac7e22ba9fb1e2f1e17f972229014314b823e77a`  
		Last Modified: Wed, 05 Aug 2020 16:37:58 GMT  
		Size: 2.8 KB (2820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d707aad8b7522509ed41150ec4346ed9757dd7b9ce23404bc8001c695c119ed`  
		Last Modified: Wed, 05 Aug 2020 16:38:04 GMT  
		Size: 21.7 MB (21665200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d43c06bab41756c280d0946332594f0835249b5879a2ca787fe5062fa8ebc02`  
		Last Modified: Wed, 05 Aug 2020 16:37:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:36f6d826e9bdfbb3eccba107c6fc15736687a229abf444979acda578cccc5eeb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98881250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ee1919fa55cc5935a28896f3767fab9527815930c9c6f77cc21140f088c922`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 04:56:26 GMT
ADD file:aaf5c6340b3d662631775fa4536c2e48e9f68b6cc8d53e18fb8fd76ae41b305e in / 
# Tue, 04 Aug 2020 04:56:28 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 07:52:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 07:53:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 01:52:11 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 01:52:17 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 01:52:18 GMT
ENV TELEGRAF_VERSION=1.15.2
# Wed, 05 Aug 2020 01:52:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 01:52:28 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 01:52:29 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 01:52:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 01:52:34 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e7cf402ee4b1ba67e92813d50297a082bbdbdd4d47f6aeb62f2316b81d5dc843`  
		Last Modified: Tue, 04 Aug 2020 05:04:56 GMT  
		Size: 45.9 MB (45869261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff6bd4a89fc21d80ca6924320f86708f35ddea71c7aa34a408a5b64257c764e`  
		Last Modified: Tue, 04 Aug 2020 08:25:56 GMT  
		Size: 7.1 MB (7097820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48f5852a753b7731e5d374567ae9b64e309805758f336c76d5f13bb67c94e20`  
		Last Modified: Tue, 04 Aug 2020 08:25:56 GMT  
		Size: 9.3 MB (9343353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3640f9f6e2a57392770dada759969ada76ad0acba79f078302ef3a69700ea37e`  
		Last Modified: Wed, 05 Aug 2020 01:53:50 GMT  
		Size: 16.2 MB (16164767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450459590b912a0d6ee32ffe8ec59f466a4aa6d4971e2076e9c7a986d8990d2e`  
		Last Modified: Wed, 05 Aug 2020 01:53:44 GMT  
		Size: 2.8 KB (2848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573fa0f49a25bf49631c97a439fa4ab576aac8b682d38c2bf6af36bd61402c89`  
		Last Modified: Wed, 05 Aug 2020 01:53:50 GMT  
		Size: 20.4 MB (20403016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6192a8cf2cd051a9b61ba2206e992aa27d10653c53bc8b11fb1acf8afa473ee8`  
		Last Modified: Wed, 05 Aug 2020 01:53:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:01a37222da1e9a7bc94281bd479c3fbc5836b77eb0d87555e38b88ae4ed44465
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104132549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659ccc87d400174d5cdd5ff92f940e269ffc8e15f3241846f2a555fc838519ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 04 Aug 2020 06:57:06 GMT
ADD file:ce999027b153d392f8a0f85e2e7a17b9279f3cf7ad0e45192378d527275f99c6 in / 
# Tue, 04 Aug 2020 06:57:08 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:10:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:10:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 08:11:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 08:11:34 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 05 Aug 2020 08:11:34 GMT
ENV TELEGRAF_VERSION=1.15.2
# Wed, 05 Aug 2020 08:11:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 05 Aug 2020 08:11:42 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 05 Aug 2020 08:11:43 GMT
COPY file:7e725b38b34580a28d521266535fcafc651af09f8af8fc6e03ef74768e1b69a2 in /entrypoint.sh 
# Wed, 05 Aug 2020 08:11:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Aug 2020 08:11:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d5517ee72007172d5b814636405254dea459120ce08f85777bb287d106a6a240`  
		Last Modified: Tue, 04 Aug 2020 07:03:41 GMT  
		Size: 49.2 MB (49175491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283897ad4463628bd259e1cbb5eb788e7df554b42ae17fc6f5d02c4a56035c2`  
		Last Modified: Tue, 04 Aug 2020 11:23:01 GMT  
		Size: 7.7 MB (7681458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3feb40d9f5fecfa098b8f7ece6c287c6fd61b114043c8b4647359120a7d943a3`  
		Last Modified: Tue, 04 Aug 2020 11:23:02 GMT  
		Size: 10.0 MB (9983917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de25b7c9c4b90ae60cb3bf5d21d5cdda40e683278598f2223e94766b9333c2f`  
		Last Modified: Wed, 05 Aug 2020 08:12:33 GMT  
		Size: 17.3 MB (17270209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482953fc118c18769e9d7a2d3513556d40569fff4794e1bcbd845c2bd9f77c21`  
		Last Modified: Wed, 05 Aug 2020 08:12:27 GMT  
		Size: 2.8 KB (2847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bb152b6321b05c80bbccfc9098925997ce73488af052b97cc43bcb2a9ac5a1`  
		Last Modified: Wed, 05 Aug 2020 08:12:34 GMT  
		Size: 20.0 MB (20018441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c689c05367c12d93d51f002d9b053e4e1b9dcad97b137d4901d18c56599a810`  
		Last Modified: Wed, 05 Aug 2020 08:12:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
