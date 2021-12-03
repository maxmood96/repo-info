## `telegraf:latest`

```console
$ docker pull telegraf@sha256:f6ae081705426f48e69db8ecfdd1d7c635584167656997a2dbff834dc20affd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:0f62fa65be36a4e2f8f111eefd6eaf8c25a6f8341ce7cc709af738d77c63d101
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121320348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cb255a1ae30a1dffa7eb1f466180c8e05a03959c83eaa91dc1dcd43c59bb7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:31 GMT
ADD file:f077e1a42fb919be2af67820782ceee3b46ffd13d7ab6949bea9921217d12813 in / 
# Thu, 02 Dec 2021 02:48:32 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:41:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Dec 2021 04:32:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 04:32:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 04:32:40 GMT
ENV TELEGRAF_VERSION=1.20.4
# Fri, 03 Dec 2021 04:32:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 03 Dec 2021 04:32:46 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 03 Dec 2021 04:32:46 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 03 Dec 2021 04:32:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 04:32:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c4cc477c22ba7abce860198107408434dd7bd73ddbaf82f1e69ab941b9979405`  
		Last Modified: Thu, 02 Dec 2021 02:54:07 GMT  
		Size: 50.4 MB (50437113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077c54d048f1f1a1f28079caa54bf5d99803f937ffe5c1dc6e207698f70b4e74`  
		Last Modified: Thu, 02 Dec 2021 03:50:46 GMT  
		Size: 7.8 MB (7833819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368544993b2deeeffdd19463cdf92ec4e39f83073de5de316f9f5c725ab403f`  
		Last Modified: Thu, 02 Dec 2021 03:50:46 GMT  
		Size: 10.0 MB (9997240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d19fc3bb1a1152e2be5e863a11ffafd241f042019bc0191614d8552ef25b3fd`  
		Last Modified: Fri, 03 Dec 2021 04:33:13 GMT  
		Size: 17.4 MB (17415385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ada106a1ddfa307bb6f3b252de34b237c4dd398272b5c71c9ae6d8fa1e56abf`  
		Last Modified: Fri, 03 Dec 2021 04:33:10 GMT  
		Size: 2.9 KB (2906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e06a28ac32f4bab638d1a5b479c51e66f381e120475b90158a7b841bb753760`  
		Last Modified: Fri, 03 Dec 2021 04:33:52 GMT  
		Size: 35.6 MB (35633654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac2e943959b3f8077504e390f9aa41fb3f518b5e350f9bd9b9c5b966e9b53a5`  
		Last Modified: Fri, 03 Dec 2021 04:33:46 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:e4a4ef230593b0769880e26fff66572c65d7a0e7491338df7003cb40ac15cf4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111646832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8105647936f3c9d10ae2b7e04016e7bb25cfd49f9de8ac2d0826a65e820d4d33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:12 GMT
ADD file:d71807613acdf86685f6d640a90e27b7b63cfe0f13d88668ee943aca089d8876 in / 
# Wed, 17 Nov 2021 02:00:13 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 02:45:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 19 Nov 2021 06:57:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 19 Nov 2021 06:57:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 19 Nov 2021 06:58:28 GMT
ENV TELEGRAF_VERSION=1.20.4
# Fri, 19 Nov 2021 06:58:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 19 Nov 2021 06:58:40 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 19 Nov 2021 06:58:41 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 19 Nov 2021 06:58:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Nov 2021 06:58:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:10acd81022d17f452439d0385615fa066b8f0ddcf3c1a803872eec5bdc6acf64`  
		Last Modified: Wed, 17 Nov 2021 02:16:00 GMT  
		Size: 45.9 MB (45918099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a9604eb6c465f658d6422593d504030155029fe0c4302451d4369030c29144`  
		Last Modified: Wed, 17 Nov 2021 03:07:14 GMT  
		Size: 7.1 MB (7125194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043b954c4f0757e89df96897cea2cf1f93c6275466008e4ba7a4b1089c7dd3d`  
		Last Modified: Wed, 17 Nov 2021 03:07:15 GMT  
		Size: 9.3 MB (9343839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f948c503612d7c3256c810d1947e6739199bedadaa86c607aaf0a20748fd2e28`  
		Last Modified: Fri, 19 Nov 2021 06:59:38 GMT  
		Size: 16.2 MB (16161406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a5c71a30ea8197d13500f671181ef00e946261de58f9df4450d46f71292b94`  
		Last Modified: Fri, 19 Nov 2021 06:59:26 GMT  
		Size: 2.9 KB (2907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6de908f25ea6225c51944cf17448323ed01586e8bd396cd2c6a31833d0b640e`  
		Last Modified: Fri, 19 Nov 2021 07:00:54 GMT  
		Size: 33.1 MB (33095155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9a22e1550f034287182d426f2f591e940c8361d8454a1d210292b6edd4ee36`  
		Last Modified: Fri, 19 Nov 2021 07:00:31 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2dcae3326239817abaaef855729f6c2efd680750e6365bda41f177c82668bf43
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116117152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dd3855686dc7b618e54c8a05c5c3cc2143e329f8b115c2f78786cb41af9795`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:20 GMT
ADD file:82c1819d8416d9d44564980e25e98a081f813bc2ee8ad2789114fe37e802848f in / 
# Thu, 02 Dec 2021 08:08:20 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:54:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:54:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Dec 2021 05:04:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 05:04:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 05:04:40 GMT
ENV TELEGRAF_VERSION=1.20.4
# Fri, 03 Dec 2021 05:04:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 03 Dec 2021 05:04:45 GMT
EXPOSE 8092/udp 8094 8125/udp
# Fri, 03 Dec 2021 05:04:46 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Fri, 03 Dec 2021 05:04:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 05:04:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:39e4f823356a9e2dbba530f9d363b4d76beaff75a13bad788d38eebeae67e5b0`  
		Last Modified: Thu, 02 Dec 2021 08:41:08 GMT  
		Size: 49.2 MB (49223045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df66cf961d4016eccee4ce9bc5dc18dcd99e9f9963e66c4980a66e6492a421b2`  
		Last Modified: Thu, 02 Dec 2021 10:03:39 GMT  
		Size: 7.7 MB (7695103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6c547e43b8b6afdfae413ba7a49c1120d0534fff63c4a242ef611d562a678c`  
		Last Modified: Thu, 02 Dec 2021 10:03:39 GMT  
		Size: 9.8 MB (9767269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad6f83cdf6241198d4e908c6f92b100cf9cc4dc5242b4d38550ca7639929981`  
		Last Modified: Fri, 03 Dec 2021 05:05:12 GMT  
		Size: 17.1 MB (17058986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5a73aa06cee308b9f2e886dd606487821f89cfcd4179ad928c98be2967203d`  
		Last Modified: Fri, 03 Dec 2021 05:05:09 GMT  
		Size: 2.9 KB (2877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a457da2a301b2827e99ea10f9db7e47ac26dbd996e3fa821834baa4101c0b0`  
		Last Modified: Fri, 03 Dec 2021 05:05:47 GMT  
		Size: 32.4 MB (32369641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1549001848a878902d2bd1aa11a741ac52eccef7d8455b81def886c9933fec6`  
		Last Modified: Fri, 03 Dec 2021 05:05:41 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
