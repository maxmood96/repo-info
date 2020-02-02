<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `influxdb`

-	[`influxdb:1.5`](#influxdb15)
-	[`influxdb:1.5.4`](#influxdb154)
-	[`influxdb:1.5.4-alpine`](#influxdb154-alpine)
-	[`influxdb:1.5.4-data`](#influxdb154-data)
-	[`influxdb:1.5.4-data-alpine`](#influxdb154-data-alpine)
-	[`influxdb:1.5.4-meta`](#influxdb154-meta)
-	[`influxdb:1.5.4-meta-alpine`](#influxdb154-meta-alpine)
-	[`influxdb:1.5-alpine`](#influxdb15-alpine)
-	[`influxdb:1.5-data`](#influxdb15-data)
-	[`influxdb:1.5-data-alpine`](#influxdb15-data-alpine)
-	[`influxdb:1.5-meta`](#influxdb15-meta)
-	[`influxdb:1.5-meta-alpine`](#influxdb15-meta-alpine)
-	[`influxdb:1.6`](#influxdb16)
-	[`influxdb:1.6.6`](#influxdb166)
-	[`influxdb:1.6.6-alpine`](#influxdb166-alpine)
-	[`influxdb:1.6.6-data`](#influxdb166-data)
-	[`influxdb:1.6.6-data-alpine`](#influxdb166-data-alpine)
-	[`influxdb:1.6.6-meta`](#influxdb166-meta)
-	[`influxdb:1.6.6-meta-alpine`](#influxdb166-meta-alpine)
-	[`influxdb:1.6-alpine`](#influxdb16-alpine)
-	[`influxdb:1.6-data`](#influxdb16-data)
-	[`influxdb:1.6-data-alpine`](#influxdb16-data-alpine)
-	[`influxdb:1.6-meta`](#influxdb16-meta)
-	[`influxdb:1.6-meta-alpine`](#influxdb16-meta-alpine)
-	[`influxdb:1.7`](#influxdb17)
-	[`influxdb:1.7.9`](#influxdb179)
-	[`influxdb:1.7.9-alpine`](#influxdb179-alpine)
-	[`influxdb:1.7.9-data`](#influxdb179-data)
-	[`influxdb:1.7.9-data-alpine`](#influxdb179-data-alpine)
-	[`influxdb:1.7.9-meta`](#influxdb179-meta)
-	[`influxdb:1.7.9-meta-alpine`](#influxdb179-meta-alpine)
-	[`influxdb:1.7-alpine`](#influxdb17-alpine)
-	[`influxdb:1.7-data`](#influxdb17-data)
-	[`influxdb:1.7-data-alpine`](#influxdb17-data-alpine)
-	[`influxdb:1.7-meta`](#influxdb17-meta)
-	[`influxdb:1.7-meta-alpine`](#influxdb17-meta-alpine)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:data`](#influxdbdata)
-	[`influxdb:data-alpine`](#influxdbdata-alpine)
-	[`influxdb:latest`](#influxdblatest)
-	[`influxdb:meta`](#influxdbmeta)
-	[`influxdb:meta-alpine`](#influxdbmeta-alpine)

## `influxdb:1.5`

```console
$ docker pull influxdb@sha256:64ae7308653b3801424c06ad8070801636b3684e6dbc17f24f93032e7bd4c394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.5` - linux; amd64

```console
$ docker pull influxdb@sha256:be6e1d983acdb55d3a7904f76f8b015f030792d6b7d359aa3669102b48338013
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83551602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68645bbae8829b1650b15b0c6c655019bd63e62e78f4ad2c02427f3f9339714a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:27:22 GMT
ENV INFLUXDB_VERSION=1.5.4
# Sun, 29 Dec 2019 06:27:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sun, 29 Dec 2019 06:27:25 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sun, 29 Dec 2019 06:27:26 GMT
EXPOSE 8086
# Sun, 29 Dec 2019 06:27:26 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:27:26 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:27:26 GMT
COPY file:9d63e46d6e9bed7502af5cddf053b5ea832d65716b7e457a74a61af74587483a in /init-influxdb.sh 
# Sun, 29 Dec 2019 06:27:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:27:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd781b922756178d78b00a8feb120774bf803f63a18aeb9f1759dc246c3d528d`  
		Last Modified: Sun, 29 Dec 2019 06:29:36 GMT  
		Size: 23.0 MB (23029030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98dd1f7ddb153d3a8b795e2821a3a69d86233f9e3669ddfbc3098297047434c9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a8d7390a00de1030805f5a1c9e726901235f7be0786d1df9e114e6f4c2bfeb`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664ba8d98df37efad2950926718770c200ccbd68886c206e577e62d19b2997c0`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.5` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:fd5929d5d9525e491928488d3970b83952f6bdbfe84b703a6e226f5c70f9cd35
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77188477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee83e32c202879ab1f45716e4ec7c852c42739ae8753add74080b59d5b06fd5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:19 GMT
ADD file:5692a55e4805d33baa21e559cc0bb86fb91422171345ddd332fa5514285a3401 in / 
# Sat, 28 Dec 2019 05:03:25 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:59:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:00:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 22:31:12 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 28 Dec 2019 22:31:15 GMT
ENV INFLUXDB_VERSION=1.5.4
# Sat, 28 Dec 2019 22:31:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sat, 28 Dec 2019 22:31:31 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 28 Dec 2019 22:31:32 GMT
EXPOSE 8086
# Sat, 28 Dec 2019 22:31:33 GMT
VOLUME [/var/lib/influxdb]
# Sat, 28 Dec 2019 22:31:34 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 28 Dec 2019 22:31:35 GMT
COPY file:9d63e46d6e9bed7502af5cddf053b5ea832d65716b7e457a74a61af74587483a in /init-influxdb.sh 
# Sat, 28 Dec 2019 22:31:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 22:31:39 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:b531ae4a39253d883a11291e842b7e1aa9dae38f9d9b77ddea55b2625ce986e3`  
		Last Modified: Sat, 28 Dec 2019 05:10:53 GMT  
		Size: 42.1 MB (42108124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22754f6fc5d5a244119c0928ebf7d851d276d7f095f07e6bf435fa7afbcab8a8`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 9.5 MB (9498197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2155e4b3456accbea4b6873247312dd288feb477ec966ed48637e031aba558`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 3.9 MB (3918728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74fbc8f56f35aa5563c51e2a9dca9b6899524e044502d812a7ba6647e9449af`  
		Last Modified: Sat, 28 Dec 2019 22:32:52 GMT  
		Size: 2.8 KB (2802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f4f8c82a967fe671a97f12597d5a078ad7a4320819ad2fda3835fb61a4d944`  
		Last Modified: Sat, 28 Dec 2019 22:32:59 GMT  
		Size: 21.7 MB (21658910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed5d41aabe6a5132d86e9f6fb0ef1fadceb0940a35ec92b898e3dda796f6baa`  
		Last Modified: Sat, 28 Dec 2019 22:32:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaddc27d96aeb4cb340a843d0c71d25be2d90bd92bdc100cd95761d0a46adc6a`  
		Last Modified: Sat, 28 Dec 2019 22:32:52 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db131996aa716c72676a166619b07b07de446ad062010621346570f7b24efd4`  
		Last Modified: Sat, 28 Dec 2019 22:32:52 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.5` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:5897d0472f72508e56582692d9f4c730ba54f1b6e14dad869870fcda7e1884f7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78024623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4373ca00f63eb80e75a114031d6d90bb7001b70fd00409fe7d77cbcf1a7b4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:01 GMT
ADD file:1618e6474dbe6462a610ce7eed99f0bfd087ea37ddfc287bbd69def5c24ede47 in / 
# Sat, 01 Feb 2020 16:43:02 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:29:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 02 Feb 2020 11:06:15 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 02 Feb 2020 11:06:17 GMT
ENV INFLUXDB_VERSION=1.5.4
# Sun, 02 Feb 2020 11:06:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sun, 02 Feb 2020 11:06:23 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sun, 02 Feb 2020 11:06:24 GMT
EXPOSE 8086
# Sun, 02 Feb 2020 11:06:25 GMT
VOLUME [/var/lib/influxdb]
# Sun, 02 Feb 2020 11:06:25 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sun, 02 Feb 2020 11:06:26 GMT
COPY file:9d63e46d6e9bed7502af5cddf053b5ea832d65716b7e457a74a61af74587483a in /init-influxdb.sh 
# Sun, 02 Feb 2020 11:06:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 11:06:27 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:df3de44c7096ba135556a1e7044f9e1feee3ef713ab96f0416f71fe78422cbf6`  
		Last Modified: Sat, 01 Feb 2020 16:48:40 GMT  
		Size: 43.2 MB (43166749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf173a01baf7d45b479bb380ece219cbf0ea52178e9b8cdc5b87891759d1122`  
		Last Modified: Sat, 01 Feb 2020 17:39:19 GMT  
		Size: 9.7 MB (9748586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3392eac7bc27f3bd5fcb024413ca55ec4115c22da3e229567d5fc03cd4ff4e4`  
		Last Modified: Sat, 01 Feb 2020 17:39:18 GMT  
		Size: 4.1 MB (4094322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde65a8145ef90dfe307279a53df204fa49964b14b50014ede6314e6cfb19397`  
		Last Modified: Sun, 02 Feb 2020 11:07:12 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec4e97415533d5299221194b5a7e7149c2d965a5dd7fa7cb044fd2fb547393`  
		Last Modified: Sun, 02 Feb 2020 11:07:18 GMT  
		Size: 21.0 MB (21010445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e07c54957f7a3a2dda52f3a616f353ea648ef08a7b7db2de76f63a4ec6609e`  
		Last Modified: Sun, 02 Feb 2020 11:07:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fb6877aa8e610d60c0294677ce1e1959c1f632d723d011c4415efd0e073390`  
		Last Modified: Sun, 02 Feb 2020 11:07:12 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d405bfb99c546c37f587535cb5445d950a3cd562e8839dd92dc8484459cb7a72`  
		Last Modified: Sun, 02 Feb 2020 11:07:12 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5.4`

```console
$ docker pull influxdb@sha256:64ae7308653b3801424c06ad8070801636b3684e6dbc17f24f93032e7bd4c394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.5.4` - linux; amd64

```console
$ docker pull influxdb@sha256:be6e1d983acdb55d3a7904f76f8b015f030792d6b7d359aa3669102b48338013
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83551602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68645bbae8829b1650b15b0c6c655019bd63e62e78f4ad2c02427f3f9339714a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:27:22 GMT
ENV INFLUXDB_VERSION=1.5.4
# Sun, 29 Dec 2019 06:27:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sun, 29 Dec 2019 06:27:25 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sun, 29 Dec 2019 06:27:26 GMT
EXPOSE 8086
# Sun, 29 Dec 2019 06:27:26 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:27:26 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:27:26 GMT
COPY file:9d63e46d6e9bed7502af5cddf053b5ea832d65716b7e457a74a61af74587483a in /init-influxdb.sh 
# Sun, 29 Dec 2019 06:27:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:27:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd781b922756178d78b00a8feb120774bf803f63a18aeb9f1759dc246c3d528d`  
		Last Modified: Sun, 29 Dec 2019 06:29:36 GMT  
		Size: 23.0 MB (23029030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98dd1f7ddb153d3a8b795e2821a3a69d86233f9e3669ddfbc3098297047434c9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a8d7390a00de1030805f5a1c9e726901235f7be0786d1df9e114e6f4c2bfeb`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664ba8d98df37efad2950926718770c200ccbd68886c206e577e62d19b2997c0`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.5.4` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:fd5929d5d9525e491928488d3970b83952f6bdbfe84b703a6e226f5c70f9cd35
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77188477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee83e32c202879ab1f45716e4ec7c852c42739ae8753add74080b59d5b06fd5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:19 GMT
ADD file:5692a55e4805d33baa21e559cc0bb86fb91422171345ddd332fa5514285a3401 in / 
# Sat, 28 Dec 2019 05:03:25 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:59:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:00:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 22:31:12 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 28 Dec 2019 22:31:15 GMT
ENV INFLUXDB_VERSION=1.5.4
# Sat, 28 Dec 2019 22:31:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sat, 28 Dec 2019 22:31:31 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 28 Dec 2019 22:31:32 GMT
EXPOSE 8086
# Sat, 28 Dec 2019 22:31:33 GMT
VOLUME [/var/lib/influxdb]
# Sat, 28 Dec 2019 22:31:34 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 28 Dec 2019 22:31:35 GMT
COPY file:9d63e46d6e9bed7502af5cddf053b5ea832d65716b7e457a74a61af74587483a in /init-influxdb.sh 
# Sat, 28 Dec 2019 22:31:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 22:31:39 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:b531ae4a39253d883a11291e842b7e1aa9dae38f9d9b77ddea55b2625ce986e3`  
		Last Modified: Sat, 28 Dec 2019 05:10:53 GMT  
		Size: 42.1 MB (42108124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22754f6fc5d5a244119c0928ebf7d851d276d7f095f07e6bf435fa7afbcab8a8`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 9.5 MB (9498197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2155e4b3456accbea4b6873247312dd288feb477ec966ed48637e031aba558`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 3.9 MB (3918728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74fbc8f56f35aa5563c51e2a9dca9b6899524e044502d812a7ba6647e9449af`  
		Last Modified: Sat, 28 Dec 2019 22:32:52 GMT  
		Size: 2.8 KB (2802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f4f8c82a967fe671a97f12597d5a078ad7a4320819ad2fda3835fb61a4d944`  
		Last Modified: Sat, 28 Dec 2019 22:32:59 GMT  
		Size: 21.7 MB (21658910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed5d41aabe6a5132d86e9f6fb0ef1fadceb0940a35ec92b898e3dda796f6baa`  
		Last Modified: Sat, 28 Dec 2019 22:32:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaddc27d96aeb4cb340a843d0c71d25be2d90bd92bdc100cd95761d0a46adc6a`  
		Last Modified: Sat, 28 Dec 2019 22:32:52 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db131996aa716c72676a166619b07b07de446ad062010621346570f7b24efd4`  
		Last Modified: Sat, 28 Dec 2019 22:32:52 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.5.4` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:5897d0472f72508e56582692d9f4c730ba54f1b6e14dad869870fcda7e1884f7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78024623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4373ca00f63eb80e75a114031d6d90bb7001b70fd00409fe7d77cbcf1a7b4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:01 GMT
ADD file:1618e6474dbe6462a610ce7eed99f0bfd087ea37ddfc287bbd69def5c24ede47 in / 
# Sat, 01 Feb 2020 16:43:02 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:29:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 02 Feb 2020 11:06:15 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 02 Feb 2020 11:06:17 GMT
ENV INFLUXDB_VERSION=1.5.4
# Sun, 02 Feb 2020 11:06:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sun, 02 Feb 2020 11:06:23 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sun, 02 Feb 2020 11:06:24 GMT
EXPOSE 8086
# Sun, 02 Feb 2020 11:06:25 GMT
VOLUME [/var/lib/influxdb]
# Sun, 02 Feb 2020 11:06:25 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sun, 02 Feb 2020 11:06:26 GMT
COPY file:9d63e46d6e9bed7502af5cddf053b5ea832d65716b7e457a74a61af74587483a in /init-influxdb.sh 
# Sun, 02 Feb 2020 11:06:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 11:06:27 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:df3de44c7096ba135556a1e7044f9e1feee3ef713ab96f0416f71fe78422cbf6`  
		Last Modified: Sat, 01 Feb 2020 16:48:40 GMT  
		Size: 43.2 MB (43166749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf173a01baf7d45b479bb380ece219cbf0ea52178e9b8cdc5b87891759d1122`  
		Last Modified: Sat, 01 Feb 2020 17:39:19 GMT  
		Size: 9.7 MB (9748586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3392eac7bc27f3bd5fcb024413ca55ec4115c22da3e229567d5fc03cd4ff4e4`  
		Last Modified: Sat, 01 Feb 2020 17:39:18 GMT  
		Size: 4.1 MB (4094322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde65a8145ef90dfe307279a53df204fa49964b14b50014ede6314e6cfb19397`  
		Last Modified: Sun, 02 Feb 2020 11:07:12 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec4e97415533d5299221194b5a7e7149c2d965a5dd7fa7cb044fd2fb547393`  
		Last Modified: Sun, 02 Feb 2020 11:07:18 GMT  
		Size: 21.0 MB (21010445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e07c54957f7a3a2dda52f3a616f353ea648ef08a7b7db2de76f63a4ec6609e`  
		Last Modified: Sun, 02 Feb 2020 11:07:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fb6877aa8e610d60c0294677ce1e1959c1f632d723d011c4415efd0e073390`  
		Last Modified: Sun, 02 Feb 2020 11:07:12 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d405bfb99c546c37f587535cb5445d950a3cd562e8839dd92dc8484459cb7a72`  
		Last Modified: Sun, 02 Feb 2020 11:07:12 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5.4-alpine`

```console
$ docker pull influxdb@sha256:8e4c6fd4173ab8788c7bbecf0f4e3fc46c380bd73795692284077fa57ec06957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5.4-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4ba2e4fffadbd511077577335f2602948f9986bd9be37283efb1b50e641576f8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27546568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6f252a585b5bba79a0e4ff0dbe6fd81f1fa6a69047a4ff83ccab54abc1c619`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:03:48 GMT
ENV INFLUXDB_VERSION=1.5.4
# Thu, 23 Jan 2020 19:03:53 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:03:53 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:03:53 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:03:53 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:03:53 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:03:54 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:03:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:03:54 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88394c2854089d5054b091622be66c81f76b1aa57aaab8a1e4fb260e6f2a4cbb`  
		Last Modified: Thu, 23 Jan 2020 19:07:10 GMT  
		Size: 22.9 MB (22916851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fc9971237ebca6230d5800910c605aa425f88e336456c4f952d3785f22236d`  
		Last Modified: Thu, 23 Jan 2020 19:07:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b417c45244d8df449455879226f05faf43924b084fffb3de3430975f03917f56`  
		Last Modified: Thu, 23 Jan 2020 19:07:01 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7397ad8bd2bc035e91075df8d70d674df7aa57e1d230556dff6a93b9d7ec370e`  
		Last Modified: Thu, 23 Jan 2020 19:07:01 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5.4-data`

```console
$ docker pull influxdb@sha256:500ce0090bbf015eb0f0730597d5700f974f74b18b3ae9b6a4b9a30fb2098d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5.4-data` - linux; amd64

```console
$ docker pull influxdb@sha256:c5c44b73869f447e0ea0185bd6609c7b73f0d808c966d6c139ee12671ba8341f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84305364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444928a362b980cf026cfc118a55aae6d7fca63b28118bd317b166ec41c9ed41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:27:34 GMT
ENV INFLUXDB_VERSION=1.5.4-c1.5.4
# Sun, 29 Dec 2019 06:27:37 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Sun, 29 Dec 2019 06:27:38 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sun, 29 Dec 2019 06:27:38 GMT
EXPOSE 8086
# Sun, 29 Dec 2019 06:27:38 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:27:38 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:27:38 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 29 Dec 2019 06:27:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:27:39 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd9b5b578826e064164b220e8eb7a01c1b4bc82456eaa125d4df9d862a39f29`  
		Last Modified: Sun, 29 Dec 2019 06:29:45 GMT  
		Size: 23.8 MB (23782737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e28dfb76625dc203cb31f06274395a1932afb2ee522fa36a458de8849f7113`  
		Last Modified: Sun, 29 Dec 2019 06:29:40 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6f91e6e7c26f3e6a6bc45439b7c88675118ffa06350018cbb6867205e2106e`  
		Last Modified: Sun, 29 Dec 2019 06:29:40 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b412e1755792087f57a343608ecef8af0f60690dfe6e2929e11ef1c125872caa`  
		Last Modified: Sun, 29 Dec 2019 06:29:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5.4-data-alpine`

```console
$ docker pull influxdb@sha256:de7ead51d90b0ea4853ef4d603cc9cc17b386d33d0d5273decaefeab25d0d86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5.4-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:0a8e496ac00fb556392e252a47b047843e176c5f38a40160f86489ceb30825c8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28299789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe04106d38b3f3d171c1ce7f48100da80cc6d63d6ee14b0820f1a70f346f1eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:02 GMT
ENV INFLUXDB_VERSION=1.5.4-c1.5.4
# Thu, 23 Jan 2020 19:04:07 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:04:07 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:04:07 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:04:07 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:04:07 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:04:07 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:04:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:04:08 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b5636523728be94f8e3e0040b406697262e4b48fde6334e9ffe248d9082401`  
		Last Modified: Thu, 23 Jan 2020 19:07:30 GMT  
		Size: 23.7 MB (23670013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb8d0867f6a6f6d4a9d64a95b07f9cd2e1e8c961ec8b75c387a1967c89ec7ec`  
		Last Modified: Thu, 23 Jan 2020 19:07:15 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54826124424838ea73c4731f23548a42ad0693312df4b0399d1368d51c44562c`  
		Last Modified: Thu, 23 Jan 2020 19:07:15 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19b6aff30df100fd8085bb178fee7e62e0cc282b763decf56cecfe747642eed`  
		Last Modified: Thu, 23 Jan 2020 19:07:15 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5.4-meta`

```console
$ docker pull influxdb@sha256:664d579d1b08ca3e3d875398bc29297a7bcd9342c358a3d745b2069f2bc9aafd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5.4-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:57a31f8c254f6df9eddf1b92055211a7e6c2029f2e6b442d1dee73a4789c9c92
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71715558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78281ea90cd8822c6327354d0454b8940843440a08597fb3718e8dda62b947d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:27:34 GMT
ENV INFLUXDB_VERSION=1.5.4-c1.5.4
# Sun, 29 Dec 2019 06:27:48 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Sun, 29 Dec 2019 06:27:49 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sun, 29 Dec 2019 06:27:49 GMT
EXPOSE 8091
# Sun, 29 Dec 2019 06:27:49 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:27:49 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:27:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:27:49 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e65dbad067506fa36cc342f9a3316717a72831ca6fbf922b69bb9d2f9bafa9`  
		Last Modified: Sun, 29 Dec 2019 06:29:51 GMT  
		Size: 11.2 MB (11194134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b54aad22494f2b310ad74729653948c7cb83ed12d0f443fed2bcd83bef8a4ec`  
		Last Modified: Sun, 29 Dec 2019 06:29:49 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06ff577ea6b058cb1299de886660024d012ebb08e640d9283214752b11e241c`  
		Last Modified: Sun, 29 Dec 2019 06:29:49 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5.4-meta-alpine`

```console
$ docker pull influxdb@sha256:6f84ba5ba10c833d9cc14b9c36541ab9657d68f1a46303784a08b691fc381154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5.4-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:77e862d69197c3b486eabc8170c199fa18dce5f81fc703d66f2fedba0d19eaf0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15779821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64e168fcf407e757b2ad9c3f9e73710a026bbe05be46a21f91d4aae930dcfa3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:02 GMT
ENV INFLUXDB_VERSION=1.5.4-c1.5.4
# Thu, 23 Jan 2020 19:04:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:04:19 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 23 Jan 2020 19:04:19 GMT
EXPOSE 8091
# Thu, 23 Jan 2020 19:04:19 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:04:19 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:04:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:04:19 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0e87069833ff629f85d2e8945f09b6a5af9aacf30af70ff537adcb22b09772`  
		Last Modified: Thu, 23 Jan 2020 19:07:43 GMT  
		Size: 11.2 MB (11151245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab027e28e6d75a43518ff2cfe15764266fc70ff97d429bcaaa8fe936585e30f5`  
		Last Modified: Thu, 23 Jan 2020 19:07:35 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2836d507107845041948aa147917bdbd6177563dee7f77b1552983df73acc37`  
		Last Modified: Thu, 23 Jan 2020 19:07:35 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5-alpine`

```console
$ docker pull influxdb@sha256:8e4c6fd4173ab8788c7bbecf0f4e3fc46c380bd73795692284077fa57ec06957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4ba2e4fffadbd511077577335f2602948f9986bd9be37283efb1b50e641576f8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27546568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6f252a585b5bba79a0e4ff0dbe6fd81f1fa6a69047a4ff83ccab54abc1c619`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:03:48 GMT
ENV INFLUXDB_VERSION=1.5.4
# Thu, 23 Jan 2020 19:03:53 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:03:53 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:03:53 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:03:53 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:03:53 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:03:54 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:03:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:03:54 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88394c2854089d5054b091622be66c81f76b1aa57aaab8a1e4fb260e6f2a4cbb`  
		Last Modified: Thu, 23 Jan 2020 19:07:10 GMT  
		Size: 22.9 MB (22916851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fc9971237ebca6230d5800910c605aa425f88e336456c4f952d3785f22236d`  
		Last Modified: Thu, 23 Jan 2020 19:07:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b417c45244d8df449455879226f05faf43924b084fffb3de3430975f03917f56`  
		Last Modified: Thu, 23 Jan 2020 19:07:01 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7397ad8bd2bc035e91075df8d70d674df7aa57e1d230556dff6a93b9d7ec370e`  
		Last Modified: Thu, 23 Jan 2020 19:07:01 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5-data`

```console
$ docker pull influxdb@sha256:500ce0090bbf015eb0f0730597d5700f974f74b18b3ae9b6a4b9a30fb2098d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5-data` - linux; amd64

```console
$ docker pull influxdb@sha256:c5c44b73869f447e0ea0185bd6609c7b73f0d808c966d6c139ee12671ba8341f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84305364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444928a362b980cf026cfc118a55aae6d7fca63b28118bd317b166ec41c9ed41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:27:34 GMT
ENV INFLUXDB_VERSION=1.5.4-c1.5.4
# Sun, 29 Dec 2019 06:27:37 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Sun, 29 Dec 2019 06:27:38 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sun, 29 Dec 2019 06:27:38 GMT
EXPOSE 8086
# Sun, 29 Dec 2019 06:27:38 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:27:38 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:27:38 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 29 Dec 2019 06:27:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:27:39 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd9b5b578826e064164b220e8eb7a01c1b4bc82456eaa125d4df9d862a39f29`  
		Last Modified: Sun, 29 Dec 2019 06:29:45 GMT  
		Size: 23.8 MB (23782737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e28dfb76625dc203cb31f06274395a1932afb2ee522fa36a458de8849f7113`  
		Last Modified: Sun, 29 Dec 2019 06:29:40 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6f91e6e7c26f3e6a6bc45439b7c88675118ffa06350018cbb6867205e2106e`  
		Last Modified: Sun, 29 Dec 2019 06:29:40 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b412e1755792087f57a343608ecef8af0f60690dfe6e2929e11ef1c125872caa`  
		Last Modified: Sun, 29 Dec 2019 06:29:41 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5-data-alpine`

```console
$ docker pull influxdb@sha256:de7ead51d90b0ea4853ef4d603cc9cc17b386d33d0d5273decaefeab25d0d86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:0a8e496ac00fb556392e252a47b047843e176c5f38a40160f86489ceb30825c8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28299789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe04106d38b3f3d171c1ce7f48100da80cc6d63d6ee14b0820f1a70f346f1eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:02 GMT
ENV INFLUXDB_VERSION=1.5.4-c1.5.4
# Thu, 23 Jan 2020 19:04:07 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:04:07 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:04:07 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:04:07 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:04:07 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:04:07 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:04:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:04:08 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b5636523728be94f8e3e0040b406697262e4b48fde6334e9ffe248d9082401`  
		Last Modified: Thu, 23 Jan 2020 19:07:30 GMT  
		Size: 23.7 MB (23670013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb8d0867f6a6f6d4a9d64a95b07f9cd2e1e8c961ec8b75c387a1967c89ec7ec`  
		Last Modified: Thu, 23 Jan 2020 19:07:15 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54826124424838ea73c4731f23548a42ad0693312df4b0399d1368d51c44562c`  
		Last Modified: Thu, 23 Jan 2020 19:07:15 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19b6aff30df100fd8085bb178fee7e62e0cc282b763decf56cecfe747642eed`  
		Last Modified: Thu, 23 Jan 2020 19:07:15 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5-meta`

```console
$ docker pull influxdb@sha256:664d579d1b08ca3e3d875398bc29297a7bcd9342c358a3d745b2069f2bc9aafd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:57a31f8c254f6df9eddf1b92055211a7e6c2029f2e6b442d1dee73a4789c9c92
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71715558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78281ea90cd8822c6327354d0454b8940843440a08597fb3718e8dda62b947d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:27:34 GMT
ENV INFLUXDB_VERSION=1.5.4-c1.5.4
# Sun, 29 Dec 2019 06:27:48 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Sun, 29 Dec 2019 06:27:49 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sun, 29 Dec 2019 06:27:49 GMT
EXPOSE 8091
# Sun, 29 Dec 2019 06:27:49 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:27:49 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:27:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:27:49 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e65dbad067506fa36cc342f9a3316717a72831ca6fbf922b69bb9d2f9bafa9`  
		Last Modified: Sun, 29 Dec 2019 06:29:51 GMT  
		Size: 11.2 MB (11194134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b54aad22494f2b310ad74729653948c7cb83ed12d0f443fed2bcd83bef8a4ec`  
		Last Modified: Sun, 29 Dec 2019 06:29:49 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06ff577ea6b058cb1299de886660024d012ebb08e640d9283214752b11e241c`  
		Last Modified: Sun, 29 Dec 2019 06:29:49 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.5-meta-alpine`

```console
$ docker pull influxdb@sha256:6f84ba5ba10c833d9cc14b9c36541ab9657d68f1a46303784a08b691fc381154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.5-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:77e862d69197c3b486eabc8170c199fa18dce5f81fc703d66f2fedba0d19eaf0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15779821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64e168fcf407e757b2ad9c3f9e73710a026bbe05be46a21f91d4aae930dcfa3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:02 GMT
ENV INFLUXDB_VERSION=1.5.4-c1.5.4
# Thu, 23 Jan 2020 19:04:18 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:04:19 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 23 Jan 2020 19:04:19 GMT
EXPOSE 8091
# Thu, 23 Jan 2020 19:04:19 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:04:19 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:04:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:04:19 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0e87069833ff629f85d2e8945f09b6a5af9aacf30af70ff537adcb22b09772`  
		Last Modified: Thu, 23 Jan 2020 19:07:43 GMT  
		Size: 11.2 MB (11151245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab027e28e6d75a43518ff2cfe15764266fc70ff97d429bcaaa8fe936585e30f5`  
		Last Modified: Thu, 23 Jan 2020 19:07:35 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2836d507107845041948aa147917bdbd6177563dee7f77b1552983df73acc37`  
		Last Modified: Thu, 23 Jan 2020 19:07:35 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6`

```console
$ docker pull influxdb@sha256:e718814da3e8c46f2963f2de59c4dccccac2eff25fb2d3c38427fc726dfa7d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.6` - linux; amd64

```console
$ docker pull influxdb@sha256:d48fbefffd35afdd5c66865f33769566937c79c0e582738779977dbe4b261251
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85831905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bc0be5c9c9568fb92d3e2a44a97e5555d79a7499606fd992dfb2aa40b7101c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:27:57 GMT
ENV INFLUXDB_VERSION=1.6.6
# Sun, 29 Dec 2019 06:28:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sun, 29 Dec 2019 06:28:01 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sun, 29 Dec 2019 06:28:01 GMT
EXPOSE 8086
# Sun, 29 Dec 2019 06:28:01 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:28:01 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:28:02 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 29 Dec 2019 06:28:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:28:02 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30da419bbe6e3d022a2b0d53f2b0ce65907fb4d34f8204deb2877d442383026e`  
		Last Modified: Sun, 29 Dec 2019 06:30:00 GMT  
		Size: 25.3 MB (25309333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47352a14247bc2f476a387c1221f686eca59ce607705dbb676443db718717f04`  
		Last Modified: Sun, 29 Dec 2019 06:29:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97996a8749c8aded725ae0d70db9ffc0276843892f181aecde69c6a6d33b430`  
		Last Modified: Sun, 29 Dec 2019 06:29:55 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e234ded3c40c35baaeb247553a001f4e2f2cfea2a8375f0759a4f3789002cc`  
		Last Modified: Sun, 29 Dec 2019 06:29:55 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.6` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:c593cff1c63334f2ba2a9a567895bffcd93acb5a8ce423132c61bda18ad611dc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79877234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0456e7c9743abb6af323771d8bd119aab3063a20b58acf9f18b8ee3833967b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:19 GMT
ADD file:5692a55e4805d33baa21e559cc0bb86fb91422171345ddd332fa5514285a3401 in / 
# Sat, 28 Dec 2019 05:03:25 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:59:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:00:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 22:31:12 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 28 Dec 2019 22:31:49 GMT
ENV INFLUXDB_VERSION=1.6.6
# Sat, 28 Dec 2019 22:31:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sat, 28 Dec 2019 22:31:58 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 28 Dec 2019 22:31:59 GMT
EXPOSE 8086
# Sat, 28 Dec 2019 22:32:00 GMT
VOLUME [/var/lib/influxdb]
# Sat, 28 Dec 2019 22:32:01 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 28 Dec 2019 22:32:02 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 28 Dec 2019 22:32:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 22:32:09 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:b531ae4a39253d883a11291e842b7e1aa9dae38f9d9b77ddea55b2625ce986e3`  
		Last Modified: Sat, 28 Dec 2019 05:10:53 GMT  
		Size: 42.1 MB (42108124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22754f6fc5d5a244119c0928ebf7d851d276d7f095f07e6bf435fa7afbcab8a8`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 9.5 MB (9498197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2155e4b3456accbea4b6873247312dd288feb477ec966ed48637e031aba558`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 3.9 MB (3918728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74fbc8f56f35aa5563c51e2a9dca9b6899524e044502d812a7ba6647e9449af`  
		Last Modified: Sat, 28 Dec 2019 22:32:52 GMT  
		Size: 2.8 KB (2802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020902c1f23e767bc3b2490620d51dfa822e398304ce1bc2f22aac3a181d7942`  
		Last Modified: Sat, 28 Dec 2019 22:33:15 GMT  
		Size: 24.3 MB (24347666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959cca8998d50302d8b1f8fe10aa4702592c02a7a4b91405474c6d8f92399f8a`  
		Last Modified: Sat, 28 Dec 2019 22:33:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d03e881d5cd633788d3d2e2d6b4a93a33864b42feb5108f5d42efb047a3c194`  
		Last Modified: Sat, 28 Dec 2019 22:33:06 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7290407f03d7c786a6fe7e9e0c8a746a627b92ed239d0f61653d8b49204a0c`  
		Last Modified: Sat, 28 Dec 2019 22:33:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.6` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b7ee3a1e0410ff8593770ae4299ce3d86344987f04163cca08755a1ff197b261
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80679139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96be67a8cbaffa7d480a36709bc8c64f0438f301442e55c6b1bc378383f6f84d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:01 GMT
ADD file:1618e6474dbe6462a610ce7eed99f0bfd087ea37ddfc287bbd69def5c24ede47 in / 
# Sat, 01 Feb 2020 16:43:02 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:29:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 02 Feb 2020 11:06:15 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 02 Feb 2020 11:06:32 GMT
ENV INFLUXDB_VERSION=1.6.6
# Sun, 02 Feb 2020 11:06:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sun, 02 Feb 2020 11:06:38 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sun, 02 Feb 2020 11:06:39 GMT
EXPOSE 8086
# Sun, 02 Feb 2020 11:06:39 GMT
VOLUME [/var/lib/influxdb]
# Sun, 02 Feb 2020 11:06:40 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sun, 02 Feb 2020 11:06:41 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 02 Feb 2020 11:06:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 11:06:42 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:df3de44c7096ba135556a1e7044f9e1feee3ef713ab96f0416f71fe78422cbf6`  
		Last Modified: Sat, 01 Feb 2020 16:48:40 GMT  
		Size: 43.2 MB (43166749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf173a01baf7d45b479bb380ece219cbf0ea52178e9b8cdc5b87891759d1122`  
		Last Modified: Sat, 01 Feb 2020 17:39:19 GMT  
		Size: 9.7 MB (9748586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3392eac7bc27f3bd5fcb024413ca55ec4115c22da3e229567d5fc03cd4ff4e4`  
		Last Modified: Sat, 01 Feb 2020 17:39:18 GMT  
		Size: 4.1 MB (4094322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde65a8145ef90dfe307279a53df204fa49964b14b50014ede6314e6cfb19397`  
		Last Modified: Sun, 02 Feb 2020 11:07:12 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe7684b9233c40a5690c5227e4ae0e38355fb3168b9cfe4d1b0b15d0934c30a`  
		Last Modified: Sun, 02 Feb 2020 11:07:32 GMT  
		Size: 23.7 MB (23664960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd8290989242f6399bc16bbfd8fcfeaee4c7905e3fa9582d2ea4c42309e8565`  
		Last Modified: Sun, 02 Feb 2020 11:07:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9400a67ac2a6b7b33ffbf1da47e8ea0a6f10ca139d574bd20c310d4cbbb6338`  
		Last Modified: Sun, 02 Feb 2020 11:07:25 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6f2210019288253002cb70c23ed84f683cf52958dc522e7e09434aa595797a`  
		Last Modified: Sun, 02 Feb 2020 11:07:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6.6`

```console
$ docker pull influxdb@sha256:e718814da3e8c46f2963f2de59c4dccccac2eff25fb2d3c38427fc726dfa7d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.6.6` - linux; amd64

```console
$ docker pull influxdb@sha256:d48fbefffd35afdd5c66865f33769566937c79c0e582738779977dbe4b261251
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85831905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bc0be5c9c9568fb92d3e2a44a97e5555d79a7499606fd992dfb2aa40b7101c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:27:57 GMT
ENV INFLUXDB_VERSION=1.6.6
# Sun, 29 Dec 2019 06:28:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sun, 29 Dec 2019 06:28:01 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sun, 29 Dec 2019 06:28:01 GMT
EXPOSE 8086
# Sun, 29 Dec 2019 06:28:01 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:28:01 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:28:02 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 29 Dec 2019 06:28:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:28:02 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30da419bbe6e3d022a2b0d53f2b0ce65907fb4d34f8204deb2877d442383026e`  
		Last Modified: Sun, 29 Dec 2019 06:30:00 GMT  
		Size: 25.3 MB (25309333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47352a14247bc2f476a387c1221f686eca59ce607705dbb676443db718717f04`  
		Last Modified: Sun, 29 Dec 2019 06:29:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97996a8749c8aded725ae0d70db9ffc0276843892f181aecde69c6a6d33b430`  
		Last Modified: Sun, 29 Dec 2019 06:29:55 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e234ded3c40c35baaeb247553a001f4e2f2cfea2a8375f0759a4f3789002cc`  
		Last Modified: Sun, 29 Dec 2019 06:29:55 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.6.6` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:c593cff1c63334f2ba2a9a567895bffcd93acb5a8ce423132c61bda18ad611dc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79877234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0456e7c9743abb6af323771d8bd119aab3063a20b58acf9f18b8ee3833967b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:19 GMT
ADD file:5692a55e4805d33baa21e559cc0bb86fb91422171345ddd332fa5514285a3401 in / 
# Sat, 28 Dec 2019 05:03:25 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:59:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:00:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 22:31:12 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 28 Dec 2019 22:31:49 GMT
ENV INFLUXDB_VERSION=1.6.6
# Sat, 28 Dec 2019 22:31:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sat, 28 Dec 2019 22:31:58 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 28 Dec 2019 22:31:59 GMT
EXPOSE 8086
# Sat, 28 Dec 2019 22:32:00 GMT
VOLUME [/var/lib/influxdb]
# Sat, 28 Dec 2019 22:32:01 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 28 Dec 2019 22:32:02 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 28 Dec 2019 22:32:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 22:32:09 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:b531ae4a39253d883a11291e842b7e1aa9dae38f9d9b77ddea55b2625ce986e3`  
		Last Modified: Sat, 28 Dec 2019 05:10:53 GMT  
		Size: 42.1 MB (42108124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22754f6fc5d5a244119c0928ebf7d851d276d7f095f07e6bf435fa7afbcab8a8`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 9.5 MB (9498197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2155e4b3456accbea4b6873247312dd288feb477ec966ed48637e031aba558`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 3.9 MB (3918728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74fbc8f56f35aa5563c51e2a9dca9b6899524e044502d812a7ba6647e9449af`  
		Last Modified: Sat, 28 Dec 2019 22:32:52 GMT  
		Size: 2.8 KB (2802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020902c1f23e767bc3b2490620d51dfa822e398304ce1bc2f22aac3a181d7942`  
		Last Modified: Sat, 28 Dec 2019 22:33:15 GMT  
		Size: 24.3 MB (24347666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959cca8998d50302d8b1f8fe10aa4702592c02a7a4b91405474c6d8f92399f8a`  
		Last Modified: Sat, 28 Dec 2019 22:33:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d03e881d5cd633788d3d2e2d6b4a93a33864b42feb5108f5d42efb047a3c194`  
		Last Modified: Sat, 28 Dec 2019 22:33:06 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7290407f03d7c786a6fe7e9e0c8a746a627b92ed239d0f61653d8b49204a0c`  
		Last Modified: Sat, 28 Dec 2019 22:33:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.6.6` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b7ee3a1e0410ff8593770ae4299ce3d86344987f04163cca08755a1ff197b261
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80679139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96be67a8cbaffa7d480a36709bc8c64f0438f301442e55c6b1bc378383f6f84d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:01 GMT
ADD file:1618e6474dbe6462a610ce7eed99f0bfd087ea37ddfc287bbd69def5c24ede47 in / 
# Sat, 01 Feb 2020 16:43:02 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:29:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 02 Feb 2020 11:06:15 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 02 Feb 2020 11:06:32 GMT
ENV INFLUXDB_VERSION=1.6.6
# Sun, 02 Feb 2020 11:06:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sun, 02 Feb 2020 11:06:38 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sun, 02 Feb 2020 11:06:39 GMT
EXPOSE 8086
# Sun, 02 Feb 2020 11:06:39 GMT
VOLUME [/var/lib/influxdb]
# Sun, 02 Feb 2020 11:06:40 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sun, 02 Feb 2020 11:06:41 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 02 Feb 2020 11:06:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 11:06:42 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:df3de44c7096ba135556a1e7044f9e1feee3ef713ab96f0416f71fe78422cbf6`  
		Last Modified: Sat, 01 Feb 2020 16:48:40 GMT  
		Size: 43.2 MB (43166749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf173a01baf7d45b479bb380ece219cbf0ea52178e9b8cdc5b87891759d1122`  
		Last Modified: Sat, 01 Feb 2020 17:39:19 GMT  
		Size: 9.7 MB (9748586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3392eac7bc27f3bd5fcb024413ca55ec4115c22da3e229567d5fc03cd4ff4e4`  
		Last Modified: Sat, 01 Feb 2020 17:39:18 GMT  
		Size: 4.1 MB (4094322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde65a8145ef90dfe307279a53df204fa49964b14b50014ede6314e6cfb19397`  
		Last Modified: Sun, 02 Feb 2020 11:07:12 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe7684b9233c40a5690c5227e4ae0e38355fb3168b9cfe4d1b0b15d0934c30a`  
		Last Modified: Sun, 02 Feb 2020 11:07:32 GMT  
		Size: 23.7 MB (23664960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd8290989242f6399bc16bbfd8fcfeaee4c7905e3fa9582d2ea4c42309e8565`  
		Last Modified: Sun, 02 Feb 2020 11:07:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9400a67ac2a6b7b33ffbf1da47e8ea0a6f10ca139d574bd20c310d4cbbb6338`  
		Last Modified: Sun, 02 Feb 2020 11:07:25 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6f2210019288253002cb70c23ed84f683cf52958dc522e7e09434aa595797a`  
		Last Modified: Sun, 02 Feb 2020 11:07:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6.6-alpine`

```console
$ docker pull influxdb@sha256:e60ab84cd8ec29d78b5d521599d8b301412c786688a6fe20b220af841ac7e39d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6.6-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5e4e97a593880e8a87bb23aa3639f9f670e09e9b7a270a2506b7e0a060a2fb90
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29819765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895b69188094ed510263d77a311bbf4ddafabbb163e03b87fcfd530b74259420`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:28 GMT
ENV INFLUXDB_VERSION=1.6.6
# Thu, 23 Jan 2020 19:04:34 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:04:35 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:04:35 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:04:35 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:04:36 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:04:36 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:04:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:04:36 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a151a3c263ad506526e5130f4a8bbc2235448102aa0718108b3ccb238f11a5`  
		Last Modified: Thu, 23 Jan 2020 19:08:04 GMT  
		Size: 25.2 MB (25190045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a05f89f09d0ed1cfaf52247a8db617df8e97f3741004b646cf0208f7b469f5c`  
		Last Modified: Thu, 23 Jan 2020 19:07:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d98e03916bb6aad744b9c054a966c996532b8a1c962c1a891b143fe2fb3a4cd`  
		Last Modified: Thu, 23 Jan 2020 19:07:49 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744cc3d6ebb5f7879f04721c401125f0f4ec928e5c6b9f040add9cde29397359`  
		Last Modified: Thu, 23 Jan 2020 19:07:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6.6-data`

```console
$ docker pull influxdb@sha256:71c947809ee0b17ad6d428607fc0116e5ddd3ce6c2fe7bf55506a0e3abb5c3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6.6-data` - linux; amd64

```console
$ docker pull influxdb@sha256:c45ff61482f472ed8a93fce4b7c580557f27d65ef9cc38ae0ce881cfc2f4674f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87094724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526f586ac37ec441e09c36278b90d6dbba98c859f975aadc9fc5f69fda832587`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:28:09 GMT
ENV INFLUXDB_VERSION=1.6.6-c1.6.6
# Sun, 29 Dec 2019 06:28:13 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Sun, 29 Dec 2019 06:28:13 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sun, 29 Dec 2019 06:28:13 GMT
EXPOSE 8086
# Sun, 29 Dec 2019 06:28:13 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:28:13 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:28:14 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 29 Dec 2019 06:28:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:28:14 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99c9a7ba6f3dac5aa45d760ca509fe804a8938e5206435a324dec333ff1f034`  
		Last Modified: Sun, 29 Dec 2019 06:30:10 GMT  
		Size: 26.6 MB (26572095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40008207ac65ad756c23e0c51baad71b41246760d772f5e8fe0fac6c5e58f42a`  
		Last Modified: Sun, 29 Dec 2019 06:30:04 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986bd611320b073a9d2141b5eab67e7101c9dd12e37f75bf9ab2e0b029a32b2c`  
		Last Modified: Sun, 29 Dec 2019 06:30:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5672d99a45f59b7aca9507411dbd898df5ea9437dada379c90a37b91a3e635c5`  
		Last Modified: Sun, 29 Dec 2019 06:30:04 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6.6-data-alpine`

```console
$ docker pull influxdb@sha256:f51fc6d7713bdc8f2c15aab1d51be52000e011625035b8ee98855070f3b1c49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6.6-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2de0016b2ef4b8b3aae9e18bbbd0c69ce264fa1c040d664c84f148ebca5e5c5b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31082210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b7416db022c81033acdb0769f087d71797e95be591ae5221e065852079f4cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:45 GMT
ENV INFLUXDB_VERSION=1.6.6-c1.6.6
# Thu, 23 Jan 2020 19:04:52 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:04:52 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:04:52 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:04:53 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:04:53 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:04:53 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:04:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:04:54 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee5a3c7ffbad06c5f2dc9cbdfe7d7f7e2dfb86669ad668682a7b447f26482a6`  
		Last Modified: Thu, 23 Jan 2020 19:08:18 GMT  
		Size: 26.5 MB (26452432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3809d3ef5db1ec9ee254ae86da4919cd2106320ad70c4079ec13e747bcf4e9d0`  
		Last Modified: Thu, 23 Jan 2020 19:08:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68df561574e02cac655e37af87f36eec1442e47592ec23533456764749f6b08c`  
		Last Modified: Thu, 23 Jan 2020 19:08:10 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c80f847536ae5085e3e2437ca2d567776548c98d908624546cb808d76967bc`  
		Last Modified: Thu, 23 Jan 2020 19:08:10 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6.6-meta`

```console
$ docker pull influxdb@sha256:75747d638e8877ac6181bcb878fa6e9f6af60aa5b11f326656bfb72c5c4dde47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6.6-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:b3a6947cbf41ca267c8fe2e50723df60631f0deaa3a4d52eff0289b76a6768b3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73070533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fef82e54377a5d379638eb209bbf71b9715e74bb369571925304b3ca23bc32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:28:09 GMT
ENV INFLUXDB_VERSION=1.6.6-c1.6.6
# Sun, 29 Dec 2019 06:28:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Sun, 29 Dec 2019 06:28:24 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sun, 29 Dec 2019 06:28:24 GMT
EXPOSE 8091
# Sun, 29 Dec 2019 06:28:24 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:28:24 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:28:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:28:25 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c2a7e1756e3c9c0c8796a2684c8fe755d5925142bb3c7deb18721ff217101e`  
		Last Modified: Sun, 29 Dec 2019 06:30:16 GMT  
		Size: 12.5 MB (12549105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974625a05cc8c1c471b040952260242b20eb90e81b484765f9279acae5ebef00`  
		Last Modified: Sun, 29 Dec 2019 06:30:13 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16fd10a3ae6c419d174fc2fb1a7ad553773bee73525c68e901ead315a910d15`  
		Last Modified: Sun, 29 Dec 2019 06:30:13 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6.6-meta-alpine`

```console
$ docker pull influxdb@sha256:f61c44d51eaa6cb19ce9e9d843ea7af742638550865de9c520bfe2830a4843c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6.6-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:df5bfa4f8a27751e5982ad0204f65a2890e507185996dd5910501655429d84e0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17133215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636882454a88a2ac32cb337b9cea0a68e6213fea058dadd5e2594b1859f76e19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:45 GMT
ENV INFLUXDB_VERSION=1.6.6-c1.6.6
# Thu, 23 Jan 2020 19:05:07 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:05:07 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 23 Jan 2020 19:05:08 GMT
EXPOSE 8091
# Thu, 23 Jan 2020 19:05:08 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:05:08 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:05:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:05:09 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1444ac986dfc2da3021e80d7f77108c243e6dd5fdc69f2fb00c7db43659f982b`  
		Last Modified: Thu, 23 Jan 2020 19:08:32 GMT  
		Size: 12.5 MB (12504639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d95a63d52ff0d2fd2bcff5cdd2bd5d68cf7aa680a6d1f465a4bb7041ff7b0`  
		Last Modified: Thu, 23 Jan 2020 19:08:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefc3206ef8d05db423379f56204ab63424a340f63f75fa7864d04550fa15922`  
		Last Modified: Thu, 23 Jan 2020 19:08:24 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6-alpine`

```console
$ docker pull influxdb@sha256:e60ab84cd8ec29d78b5d521599d8b301412c786688a6fe20b220af841ac7e39d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5e4e97a593880e8a87bb23aa3639f9f670e09e9b7a270a2506b7e0a060a2fb90
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29819765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895b69188094ed510263d77a311bbf4ddafabbb163e03b87fcfd530b74259420`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:28 GMT
ENV INFLUXDB_VERSION=1.6.6
# Thu, 23 Jan 2020 19:04:34 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:04:35 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:04:35 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:04:35 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:04:36 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:04:36 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:04:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:04:36 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a151a3c263ad506526e5130f4a8bbc2235448102aa0718108b3ccb238f11a5`  
		Last Modified: Thu, 23 Jan 2020 19:08:04 GMT  
		Size: 25.2 MB (25190045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a05f89f09d0ed1cfaf52247a8db617df8e97f3741004b646cf0208f7b469f5c`  
		Last Modified: Thu, 23 Jan 2020 19:07:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d98e03916bb6aad744b9c054a966c996532b8a1c962c1a891b143fe2fb3a4cd`  
		Last Modified: Thu, 23 Jan 2020 19:07:49 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744cc3d6ebb5f7879f04721c401125f0f4ec928e5c6b9f040add9cde29397359`  
		Last Modified: Thu, 23 Jan 2020 19:07:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6-data`

```console
$ docker pull influxdb@sha256:71c947809ee0b17ad6d428607fc0116e5ddd3ce6c2fe7bf55506a0e3abb5c3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6-data` - linux; amd64

```console
$ docker pull influxdb@sha256:c45ff61482f472ed8a93fce4b7c580557f27d65ef9cc38ae0ce881cfc2f4674f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87094724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526f586ac37ec441e09c36278b90d6dbba98c859f975aadc9fc5f69fda832587`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:28:09 GMT
ENV INFLUXDB_VERSION=1.6.6-c1.6.6
# Sun, 29 Dec 2019 06:28:13 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Sun, 29 Dec 2019 06:28:13 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sun, 29 Dec 2019 06:28:13 GMT
EXPOSE 8086
# Sun, 29 Dec 2019 06:28:13 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:28:13 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:28:14 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 29 Dec 2019 06:28:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:28:14 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99c9a7ba6f3dac5aa45d760ca509fe804a8938e5206435a324dec333ff1f034`  
		Last Modified: Sun, 29 Dec 2019 06:30:10 GMT  
		Size: 26.6 MB (26572095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40008207ac65ad756c23e0c51baad71b41246760d772f5e8fe0fac6c5e58f42a`  
		Last Modified: Sun, 29 Dec 2019 06:30:04 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986bd611320b073a9d2141b5eab67e7101c9dd12e37f75bf9ab2e0b029a32b2c`  
		Last Modified: Sun, 29 Dec 2019 06:30:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5672d99a45f59b7aca9507411dbd898df5ea9437dada379c90a37b91a3e635c5`  
		Last Modified: Sun, 29 Dec 2019 06:30:04 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6-data-alpine`

```console
$ docker pull influxdb@sha256:f51fc6d7713bdc8f2c15aab1d51be52000e011625035b8ee98855070f3b1c49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2de0016b2ef4b8b3aae9e18bbbd0c69ce264fa1c040d664c84f148ebca5e5c5b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31082210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b7416db022c81033acdb0769f087d71797e95be591ae5221e065852079f4cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:45 GMT
ENV INFLUXDB_VERSION=1.6.6-c1.6.6
# Thu, 23 Jan 2020 19:04:52 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:04:52 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:04:52 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:04:53 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:04:53 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:04:53 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:04:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:04:54 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee5a3c7ffbad06c5f2dc9cbdfe7d7f7e2dfb86669ad668682a7b447f26482a6`  
		Last Modified: Thu, 23 Jan 2020 19:08:18 GMT  
		Size: 26.5 MB (26452432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3809d3ef5db1ec9ee254ae86da4919cd2106320ad70c4079ec13e747bcf4e9d0`  
		Last Modified: Thu, 23 Jan 2020 19:08:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68df561574e02cac655e37af87f36eec1442e47592ec23533456764749f6b08c`  
		Last Modified: Thu, 23 Jan 2020 19:08:10 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c80f847536ae5085e3e2437ca2d567776548c98d908624546cb808d76967bc`  
		Last Modified: Thu, 23 Jan 2020 19:08:10 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6-meta`

```console
$ docker pull influxdb@sha256:75747d638e8877ac6181bcb878fa6e9f6af60aa5b11f326656bfb72c5c4dde47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:b3a6947cbf41ca267c8fe2e50723df60631f0deaa3a4d52eff0289b76a6768b3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73070533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fef82e54377a5d379638eb209bbf71b9715e74bb369571925304b3ca23bc32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:28:09 GMT
ENV INFLUXDB_VERSION=1.6.6-c1.6.6
# Sun, 29 Dec 2019 06:28:24 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Sun, 29 Dec 2019 06:28:24 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sun, 29 Dec 2019 06:28:24 GMT
EXPOSE 8091
# Sun, 29 Dec 2019 06:28:24 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:28:24 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:28:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:28:25 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c2a7e1756e3c9c0c8796a2684c8fe755d5925142bb3c7deb18721ff217101e`  
		Last Modified: Sun, 29 Dec 2019 06:30:16 GMT  
		Size: 12.5 MB (12549105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974625a05cc8c1c471b040952260242b20eb90e81b484765f9279acae5ebef00`  
		Last Modified: Sun, 29 Dec 2019 06:30:13 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16fd10a3ae6c419d174fc2fb1a7ad553773bee73525c68e901ead315a910d15`  
		Last Modified: Sun, 29 Dec 2019 06:30:13 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.6-meta-alpine`

```console
$ docker pull influxdb@sha256:f61c44d51eaa6cb19ce9e9d843ea7af742638550865de9c520bfe2830a4843c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.6-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:df5bfa4f8a27751e5982ad0204f65a2890e507185996dd5910501655429d84e0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17133215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636882454a88a2ac32cb337b9cea0a68e6213fea058dadd5e2594b1859f76e19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:04:45 GMT
ENV INFLUXDB_VERSION=1.6.6-c1.6.6
# Thu, 23 Jan 2020 19:05:07 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:05:07 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 23 Jan 2020 19:05:08 GMT
EXPOSE 8091
# Thu, 23 Jan 2020 19:05:08 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:05:08 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:05:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:05:09 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1444ac986dfc2da3021e80d7f77108c243e6dd5fdc69f2fb00c7db43659f982b`  
		Last Modified: Thu, 23 Jan 2020 19:08:32 GMT  
		Size: 12.5 MB (12504639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d95a63d52ff0d2fd2bcff5cdd2bd5d68cf7aa680a6d1f465a4bb7041ff7b0`  
		Last Modified: Thu, 23 Jan 2020 19:08:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefc3206ef8d05db423379f56204ab63424a340f63f75fa7864d04550fa15922`  
		Last Modified: Thu, 23 Jan 2020 19:08:24 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7`

```console
$ docker pull influxdb@sha256:ffebb633e8687bbbf532fdaae15b77eede76c9c648a5be1ecb03b399c179c488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7` - linux; amd64

```console
$ docker pull influxdb@sha256:13f33ed5731bf1c367af2883da07ee221b3d824defd197bdfd08ceb5b6fe89fe
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124601200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30239b6d566444bce9e784d219b7bcf1d5bce1afae9f2415ffce9e14cc181433`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:28:32 GMT
ENV INFLUXDB_VERSION=1.7.9
# Sun, 29 Dec 2019 06:28:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sun, 29 Dec 2019 06:28:40 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sun, 29 Dec 2019 06:28:40 GMT
EXPOSE 8086
# Sun, 29 Dec 2019 06:28:40 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:28:40 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:28:40 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 29 Dec 2019 06:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:28:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750868d0ab2b42433705cc20081242d05642ffade36624525f71c57c396ce4d5`  
		Last Modified: Sun, 29 Dec 2019 06:30:30 GMT  
		Size: 64.1 MB (64078627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d98645d729ddaed0c07fa36d92cf3d3a8ba23f0f4adcf3afa569fa6211a1e7`  
		Last Modified: Sun, 29 Dec 2019 06:30:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bd5f153b8d6f3db65f0966dfeaeb3665658bc071c424416c01de6c6e4ea12e`  
		Last Modified: Sun, 29 Dec 2019 06:30:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f458001f5cb1d481787a16c62de8411e5f8e79d6f40abffe37cfc92677551283`  
		Last Modified: Sun, 29 Dec 2019 06:30:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:6f3d5a4206e067c6044bbe3cb2ef5d257e2a4e1a7e2a1d5f1c96b86edcd3c529
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116153019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9386ab7cb9ca9f58a1e20e72fa561de761d7444b1b04f6518bbb841ab89a0a16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:19 GMT
ADD file:5692a55e4805d33baa21e559cc0bb86fb91422171345ddd332fa5514285a3401 in / 
# Sat, 28 Dec 2019 05:03:25 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:59:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:00:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 22:31:12 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 28 Dec 2019 22:32:16 GMT
ENV INFLUXDB_VERSION=1.7.9
# Sat, 28 Dec 2019 22:32:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sat, 28 Dec 2019 22:32:32 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 28 Dec 2019 22:32:33 GMT
EXPOSE 8086
# Sat, 28 Dec 2019 22:32:34 GMT
VOLUME [/var/lib/influxdb]
# Sat, 28 Dec 2019 22:32:35 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 28 Dec 2019 22:32:36 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 28 Dec 2019 22:32:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 22:32:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:b531ae4a39253d883a11291e842b7e1aa9dae38f9d9b77ddea55b2625ce986e3`  
		Last Modified: Sat, 28 Dec 2019 05:10:53 GMT  
		Size: 42.1 MB (42108124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22754f6fc5d5a244119c0928ebf7d851d276d7f095f07e6bf435fa7afbcab8a8`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 9.5 MB (9498197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2155e4b3456accbea4b6873247312dd288feb477ec966ed48637e031aba558`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 3.9 MB (3918728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74fbc8f56f35aa5563c51e2a9dca9b6899524e044502d812a7ba6647e9449af`  
		Last Modified: Sat, 28 Dec 2019 22:32:52 GMT  
		Size: 2.8 KB (2802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80159293deebc34af54888faedc28abd12bf3071eb269dd8b7dff608338e3de5`  
		Last Modified: Sat, 28 Dec 2019 22:33:38 GMT  
		Size: 60.6 MB (60623453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2646782f025a8df2d3843af35f5056f1ce1f09bc95b1d4cb0e1aab30b4fcab6`  
		Last Modified: Sat, 28 Dec 2019 22:33:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf200223c03eedf7cde1432a96d6fe4fc0bf00fdcd3cd310c2843bb1beb23bdb`  
		Last Modified: Sat, 28 Dec 2019 22:33:22 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7bf79b2957e32b043378643aee8ec72e2d50573519c94335e2182429a923a6`  
		Last Modified: Sat, 28 Dec 2019 22:33:22 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:08fcd09b2f430d8f49e5cc1ec33b8e11120688d421d2715f037974f81a538a20
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117132805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f0618279fcd0fadb8b20ce70b686bbed61b23e5ed8f56a08147bf1f6b655fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:01 GMT
ADD file:1618e6474dbe6462a610ce7eed99f0bfd087ea37ddfc287bbd69def5c24ede47 in / 
# Sat, 01 Feb 2020 16:43:02 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:29:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 02 Feb 2020 11:06:15 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 02 Feb 2020 11:06:48 GMT
ENV INFLUXDB_VERSION=1.7.9
# Sun, 02 Feb 2020 11:06:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sun, 02 Feb 2020 11:06:58 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sun, 02 Feb 2020 11:06:59 GMT
EXPOSE 8086
# Sun, 02 Feb 2020 11:06:59 GMT
VOLUME [/var/lib/influxdb]
# Sun, 02 Feb 2020 11:07:00 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sun, 02 Feb 2020 11:07:00 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 02 Feb 2020 11:07:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 11:07:02 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:df3de44c7096ba135556a1e7044f9e1feee3ef713ab96f0416f71fe78422cbf6`  
		Last Modified: Sat, 01 Feb 2020 16:48:40 GMT  
		Size: 43.2 MB (43166749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf173a01baf7d45b479bb380ece219cbf0ea52178e9b8cdc5b87891759d1122`  
		Last Modified: Sat, 01 Feb 2020 17:39:19 GMT  
		Size: 9.7 MB (9748586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3392eac7bc27f3bd5fcb024413ca55ec4115c22da3e229567d5fc03cd4ff4e4`  
		Last Modified: Sat, 01 Feb 2020 17:39:18 GMT  
		Size: 4.1 MB (4094322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde65a8145ef90dfe307279a53df204fa49964b14b50014ede6314e6cfb19397`  
		Last Modified: Sun, 02 Feb 2020 11:07:12 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a768f38cf9405d857c8a5ef871661c9e7c4d4d9199da3284adea507adb89d59`  
		Last Modified: Sun, 02 Feb 2020 11:07:54 GMT  
		Size: 60.1 MB (60118628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5d4130725ae5650df1a864df1dbc0e79dd427c0f8fdeabc0dd8aafe0e9930a`  
		Last Modified: Sun, 02 Feb 2020 11:07:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee4f315db6d4214c07e621be52a57fb91c7ceeaf240290d58f36a153816bef8`  
		Last Modified: Sun, 02 Feb 2020 11:07:38 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101a642eb058840e738465178e38eeb41abc35bcdb9130f6576ee4a035381080`  
		Last Modified: Sun, 02 Feb 2020 11:07:38 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.9`

```console
$ docker pull influxdb@sha256:ffebb633e8687bbbf532fdaae15b77eede76c9c648a5be1ecb03b399c179c488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:1.7.9` - linux; amd64

```console
$ docker pull influxdb@sha256:13f33ed5731bf1c367af2883da07ee221b3d824defd197bdfd08ceb5b6fe89fe
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124601200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30239b6d566444bce9e784d219b7bcf1d5bce1afae9f2415ffce9e14cc181433`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:28:32 GMT
ENV INFLUXDB_VERSION=1.7.9
# Sun, 29 Dec 2019 06:28:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sun, 29 Dec 2019 06:28:40 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sun, 29 Dec 2019 06:28:40 GMT
EXPOSE 8086
# Sun, 29 Dec 2019 06:28:40 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:28:40 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:28:40 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 29 Dec 2019 06:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:28:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750868d0ab2b42433705cc20081242d05642ffade36624525f71c57c396ce4d5`  
		Last Modified: Sun, 29 Dec 2019 06:30:30 GMT  
		Size: 64.1 MB (64078627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d98645d729ddaed0c07fa36d92cf3d3a8ba23f0f4adcf3afa569fa6211a1e7`  
		Last Modified: Sun, 29 Dec 2019 06:30:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bd5f153b8d6f3db65f0966dfeaeb3665658bc071c424416c01de6c6e4ea12e`  
		Last Modified: Sun, 29 Dec 2019 06:30:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f458001f5cb1d481787a16c62de8411e5f8e79d6f40abffe37cfc92677551283`  
		Last Modified: Sun, 29 Dec 2019 06:30:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.9` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:6f3d5a4206e067c6044bbe3cb2ef5d257e2a4e1a7e2a1d5f1c96b86edcd3c529
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116153019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9386ab7cb9ca9f58a1e20e72fa561de761d7444b1b04f6518bbb841ab89a0a16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:19 GMT
ADD file:5692a55e4805d33baa21e559cc0bb86fb91422171345ddd332fa5514285a3401 in / 
# Sat, 28 Dec 2019 05:03:25 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:59:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:00:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 22:31:12 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 28 Dec 2019 22:32:16 GMT
ENV INFLUXDB_VERSION=1.7.9
# Sat, 28 Dec 2019 22:32:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sat, 28 Dec 2019 22:32:32 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 28 Dec 2019 22:32:33 GMT
EXPOSE 8086
# Sat, 28 Dec 2019 22:32:34 GMT
VOLUME [/var/lib/influxdb]
# Sat, 28 Dec 2019 22:32:35 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 28 Dec 2019 22:32:36 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 28 Dec 2019 22:32:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 22:32:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:b531ae4a39253d883a11291e842b7e1aa9dae38f9d9b77ddea55b2625ce986e3`  
		Last Modified: Sat, 28 Dec 2019 05:10:53 GMT  
		Size: 42.1 MB (42108124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22754f6fc5d5a244119c0928ebf7d851d276d7f095f07e6bf435fa7afbcab8a8`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 9.5 MB (9498197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2155e4b3456accbea4b6873247312dd288feb477ec966ed48637e031aba558`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 3.9 MB (3918728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74fbc8f56f35aa5563c51e2a9dca9b6899524e044502d812a7ba6647e9449af`  
		Last Modified: Sat, 28 Dec 2019 22:32:52 GMT  
		Size: 2.8 KB (2802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80159293deebc34af54888faedc28abd12bf3071eb269dd8b7dff608338e3de5`  
		Last Modified: Sat, 28 Dec 2019 22:33:38 GMT  
		Size: 60.6 MB (60623453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2646782f025a8df2d3843af35f5056f1ce1f09bc95b1d4cb0e1aab30b4fcab6`  
		Last Modified: Sat, 28 Dec 2019 22:33:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf200223c03eedf7cde1432a96d6fe4fc0bf00fdcd3cd310c2843bb1beb23bdb`  
		Last Modified: Sat, 28 Dec 2019 22:33:22 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7bf79b2957e32b043378643aee8ec72e2d50573519c94335e2182429a923a6`  
		Last Modified: Sat, 28 Dec 2019 22:33:22 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:1.7.9` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:08fcd09b2f430d8f49e5cc1ec33b8e11120688d421d2715f037974f81a538a20
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117132805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f0618279fcd0fadb8b20ce70b686bbed61b23e5ed8f56a08147bf1f6b655fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:01 GMT
ADD file:1618e6474dbe6462a610ce7eed99f0bfd087ea37ddfc287bbd69def5c24ede47 in / 
# Sat, 01 Feb 2020 16:43:02 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:29:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 02 Feb 2020 11:06:15 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 02 Feb 2020 11:06:48 GMT
ENV INFLUXDB_VERSION=1.7.9
# Sun, 02 Feb 2020 11:06:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sun, 02 Feb 2020 11:06:58 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sun, 02 Feb 2020 11:06:59 GMT
EXPOSE 8086
# Sun, 02 Feb 2020 11:06:59 GMT
VOLUME [/var/lib/influxdb]
# Sun, 02 Feb 2020 11:07:00 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sun, 02 Feb 2020 11:07:00 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 02 Feb 2020 11:07:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 11:07:02 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:df3de44c7096ba135556a1e7044f9e1feee3ef713ab96f0416f71fe78422cbf6`  
		Last Modified: Sat, 01 Feb 2020 16:48:40 GMT  
		Size: 43.2 MB (43166749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf173a01baf7d45b479bb380ece219cbf0ea52178e9b8cdc5b87891759d1122`  
		Last Modified: Sat, 01 Feb 2020 17:39:19 GMT  
		Size: 9.7 MB (9748586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3392eac7bc27f3bd5fcb024413ca55ec4115c22da3e229567d5fc03cd4ff4e4`  
		Last Modified: Sat, 01 Feb 2020 17:39:18 GMT  
		Size: 4.1 MB (4094322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde65a8145ef90dfe307279a53df204fa49964b14b50014ede6314e6cfb19397`  
		Last Modified: Sun, 02 Feb 2020 11:07:12 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a768f38cf9405d857c8a5ef871661c9e7c4d4d9199da3284adea507adb89d59`  
		Last Modified: Sun, 02 Feb 2020 11:07:54 GMT  
		Size: 60.1 MB (60118628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5d4130725ae5650df1a864df1dbc0e79dd427c0f8fdeabc0dd8aafe0e9930a`  
		Last Modified: Sun, 02 Feb 2020 11:07:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee4f315db6d4214c07e621be52a57fb91c7ceeaf240290d58f36a153816bef8`  
		Last Modified: Sun, 02 Feb 2020 11:07:38 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101a642eb058840e738465178e38eeb41abc35bcdb9130f6576ee4a035381080`  
		Last Modified: Sun, 02 Feb 2020 11:07:38 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.9-alpine`

```console
$ docker pull influxdb@sha256:a881bfd6d054ae96e0a9669da1b38c70144b443c2480b195328c8751b07435a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.9-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:bc7547720eb71080dafbe914948fe69e3e54af7d213720742b004b8734597ed3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68514959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d066753d5076f97093b0413b3af936ca251ed6317ed4b8e825e111e3ddcad7b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:05:18 GMT
ENV INFLUXDB_VERSION=1.7.9
# Thu, 23 Jan 2020 19:05:29 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:05:30 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:05:30 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:05:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:05:30 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:05:31 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:05:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:05:31 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d218467912abf62e1cd393acb1624443c7ff3172f0a6af7ea7305f08299428`  
		Last Modified: Thu, 23 Jan 2020 19:09:15 GMT  
		Size: 63.9 MB (63885240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12383a31bf0090401b7b255d852b9933d2efbae1d71266f6b6ae1282601edd09`  
		Last Modified: Thu, 23 Jan 2020 19:08:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2e6e59d80a3f4b471e33b68df37295b7f67cf72d977c9465296728721f1386`  
		Last Modified: Thu, 23 Jan 2020 19:08:38 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40749feb0df7c4bbc95d63eb2303aef3ffaeb51982dbd03306056fda86826656`  
		Last Modified: Thu, 23 Jan 2020 19:08:38 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.9-data`

```console
$ docker pull influxdb@sha256:4ddf5fb7da3f7246e48703507a52fac709cae4991adedad52f81e1af7900333e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:57cdf9a41cd906ac2310c973d7148e99c51e7980f6bd4d86e538132ebb5da668
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148393207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a615427926c193674d5b91ce77c1dc37bdbcc365b88f754df1f551e27f0ad62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:28:49 GMT
ENV INFLUXDB_VERSION=1.7.9-c1.7.9
# Sun, 29 Dec 2019 06:28:58 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Sun, 29 Dec 2019 06:28:59 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sun, 29 Dec 2019 06:28:59 GMT
EXPOSE 8086
# Sun, 29 Dec 2019 06:28:59 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:28:59 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:28:59 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 29 Dec 2019 06:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:29:00 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1664952a037d5402a4308e43a84fb2c5bacd6db6d56fa62c4a6083884030d181`  
		Last Modified: Sun, 29 Dec 2019 06:30:48 GMT  
		Size: 87.9 MB (87870575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f41c229695736d78455e0ff175d3e008c640e243384a4b0f71237b94510de3`  
		Last Modified: Sun, 29 Dec 2019 06:30:35 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10245fe741944c997011e2eb9e1e05214057716b71779347c79f32926c9b075`  
		Last Modified: Sun, 29 Dec 2019 06:30:35 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a8bde191a956fadeedc4b8086eb2f3ce254f938d9a30faafd99ba22336c276`  
		Last Modified: Sun, 29 Dec 2019 06:30:35 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.9-data-alpine`

```console
$ docker pull influxdb@sha256:f0dd6bb327087a283c78b7e65f7e93e0b4f9838188e95272dd4d7cd99aa0b0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:aef6f1a0b2f9bd78cf6f829731067f0c1473debf2704adf0a100dfe39353a45d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92253550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01619e7ca41394223b57f6e234b259438bb55f2cd7895deb08c0e7ae2bdccb4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:05:40 GMT
ENV INFLUXDB_VERSION=1.7.9-c1.7.9
# Thu, 23 Jan 2020 19:05:56 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:05:56 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:05:56 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:05:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:05:57 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:05:57 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:05:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945860f7f362c3f0c4ca173502f7357f4bd11da518e63157172d962cac202822`  
		Last Modified: Thu, 23 Jan 2020 19:10:09 GMT  
		Size: 87.6 MB (87623773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48d098bf00bf9fd66c31ac5573d78e18d818f2af4e1fd23963b6afd87e8aba5`  
		Last Modified: Thu, 23 Jan 2020 19:09:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5af9859c16f3d3b8f91016c0943ddbd4f6251c8e2a7880d368793925939338`  
		Last Modified: Thu, 23 Jan 2020 19:09:22 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448822405007cb2b61d086e1995ba31ce9961ef4c913e466603666d2e4a524d8`  
		Last Modified: Thu, 23 Jan 2020 19:09:21 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.9-meta`

```console
$ docker pull influxdb@sha256:4a24e768612c7a919f0dbddb7ad0fbe053e851965b24a7721d2e0d7188ee6d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c29f2fda2fe60adcb728a7f0bb4438cec14b6d4340a8824f82538ac334f2474a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83632722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc55042149f8c769f4a4d0dff3fdc7af04c1c4ecd5d997d66f1947a83ad04ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:28:49 GMT
ENV INFLUXDB_VERSION=1.7.9-c1.7.9
# Sun, 29 Dec 2019 06:29:11 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Sun, 29 Dec 2019 06:29:11 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sun, 29 Dec 2019 06:29:11 GMT
EXPOSE 8091
# Sun, 29 Dec 2019 06:29:11 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:29:11 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:29:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:29:12 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959e4fc8e7e5f1e5ab8933a44756baca38d03367fcb64ce390ac5bfda728593d`  
		Last Modified: Sun, 29 Dec 2019 06:30:56 GMT  
		Size: 23.1 MB (23111296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157f5ff977a61a4741a6f29526e7e2704ab8fa4dbfd0a2f9d0b91d12e6310e82`  
		Last Modified: Sun, 29 Dec 2019 06:30:52 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d0332bc8709680545a1c948edb00d8997c586be0c98ca6555046bfbf9db8e1`  
		Last Modified: Sun, 29 Dec 2019 06:30:53 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7.9-meta-alpine`

```console
$ docker pull influxdb@sha256:2698eb235a7d511806afa90170f36042daf1c1781f23d17d0477146290fd1680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:55e3a53d0a1f916d645e9d6b2e836ae52f9e022e58f0140b611c286f1841fc35
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27667539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71940ce7e5292095e4b97298e83867f126f12866aacb7041faeef5c873ec2068`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:05:40 GMT
ENV INFLUXDB_VERSION=1.7.9-c1.7.9
# Thu, 23 Jan 2020 19:06:15 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:06:15 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 23 Jan 2020 19:06:16 GMT
EXPOSE 8091
# Thu, 23 Jan 2020 19:06:16 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:06:16 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:06:17 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1201b89c275e51d5ea3297ef0f864075cf880dc9657b2aac87262b1dfb0cd9`  
		Last Modified: Thu, 23 Jan 2020 19:10:29 GMT  
		Size: 23.0 MB (23038963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831486b4a2e07cc7b242a6ca828ff04a4b237d93d23dc31a05fe171693fa8601`  
		Last Modified: Thu, 23 Jan 2020 19:10:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436b73eccb9dcbcc4d58635426554f6addfcbfd851e641e76ea351593e07526f`  
		Last Modified: Thu, 23 Jan 2020 19:10:16 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-alpine`

```console
$ docker pull influxdb@sha256:a881bfd6d054ae96e0a9669da1b38c70144b443c2480b195328c8751b07435a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:bc7547720eb71080dafbe914948fe69e3e54af7d213720742b004b8734597ed3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68514959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d066753d5076f97093b0413b3af936ca251ed6317ed4b8e825e111e3ddcad7b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:05:18 GMT
ENV INFLUXDB_VERSION=1.7.9
# Thu, 23 Jan 2020 19:05:29 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:05:30 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:05:30 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:05:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:05:30 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:05:31 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:05:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:05:31 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d218467912abf62e1cd393acb1624443c7ff3172f0a6af7ea7305f08299428`  
		Last Modified: Thu, 23 Jan 2020 19:09:15 GMT  
		Size: 63.9 MB (63885240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12383a31bf0090401b7b255d852b9933d2efbae1d71266f6b6ae1282601edd09`  
		Last Modified: Thu, 23 Jan 2020 19:08:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2e6e59d80a3f4b471e33b68df37295b7f67cf72d977c9465296728721f1386`  
		Last Modified: Thu, 23 Jan 2020 19:08:38 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40749feb0df7c4bbc95d63eb2303aef3ffaeb51982dbd03306056fda86826656`  
		Last Modified: Thu, 23 Jan 2020 19:08:38 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data`

```console
$ docker pull influxdb@sha256:4ddf5fb7da3f7246e48703507a52fac709cae4991adedad52f81e1af7900333e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data` - linux; amd64

```console
$ docker pull influxdb@sha256:57cdf9a41cd906ac2310c973d7148e99c51e7980f6bd4d86e538132ebb5da668
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148393207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a615427926c193674d5b91ce77c1dc37bdbcc365b88f754df1f551e27f0ad62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:28:49 GMT
ENV INFLUXDB_VERSION=1.7.9-c1.7.9
# Sun, 29 Dec 2019 06:28:58 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Sun, 29 Dec 2019 06:28:59 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sun, 29 Dec 2019 06:28:59 GMT
EXPOSE 8086
# Sun, 29 Dec 2019 06:28:59 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:28:59 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:28:59 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 29 Dec 2019 06:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:29:00 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1664952a037d5402a4308e43a84fb2c5bacd6db6d56fa62c4a6083884030d181`  
		Last Modified: Sun, 29 Dec 2019 06:30:48 GMT  
		Size: 87.9 MB (87870575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f41c229695736d78455e0ff175d3e008c640e243384a4b0f71237b94510de3`  
		Last Modified: Sun, 29 Dec 2019 06:30:35 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10245fe741944c997011e2eb9e1e05214057716b71779347c79f32926c9b075`  
		Last Modified: Sun, 29 Dec 2019 06:30:35 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a8bde191a956fadeedc4b8086eb2f3ce254f938d9a30faafd99ba22336c276`  
		Last Modified: Sun, 29 Dec 2019 06:30:35 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-data-alpine`

```console
$ docker pull influxdb@sha256:f0dd6bb327087a283c78b7e65f7e93e0b4f9838188e95272dd4d7cd99aa0b0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:aef6f1a0b2f9bd78cf6f829731067f0c1473debf2704adf0a100dfe39353a45d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92253550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01619e7ca41394223b57f6e234b259438bb55f2cd7895deb08c0e7ae2bdccb4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:05:40 GMT
ENV INFLUXDB_VERSION=1.7.9-c1.7.9
# Thu, 23 Jan 2020 19:05:56 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:05:56 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:05:56 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:05:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:05:57 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:05:57 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:05:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945860f7f362c3f0c4ca173502f7357f4bd11da518e63157172d962cac202822`  
		Last Modified: Thu, 23 Jan 2020 19:10:09 GMT  
		Size: 87.6 MB (87623773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48d098bf00bf9fd66c31ac5573d78e18d818f2af4e1fd23963b6afd87e8aba5`  
		Last Modified: Thu, 23 Jan 2020 19:09:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5af9859c16f3d3b8f91016c0943ddbd4f6251c8e2a7880d368793925939338`  
		Last Modified: Thu, 23 Jan 2020 19:09:22 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448822405007cb2b61d086e1995ba31ce9961ef4c913e466603666d2e4a524d8`  
		Last Modified: Thu, 23 Jan 2020 19:09:21 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta`

```console
$ docker pull influxdb@sha256:4a24e768612c7a919f0dbddb7ad0fbe053e851965b24a7721d2e0d7188ee6d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c29f2fda2fe60adcb728a7f0bb4438cec14b6d4340a8824f82538ac334f2474a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83632722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc55042149f8c769f4a4d0dff3fdc7af04c1c4ecd5d997d66f1947a83ad04ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:28:49 GMT
ENV INFLUXDB_VERSION=1.7.9-c1.7.9
# Sun, 29 Dec 2019 06:29:11 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Sun, 29 Dec 2019 06:29:11 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sun, 29 Dec 2019 06:29:11 GMT
EXPOSE 8091
# Sun, 29 Dec 2019 06:29:11 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:29:11 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:29:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:29:12 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959e4fc8e7e5f1e5ab8933a44756baca38d03367fcb64ce390ac5bfda728593d`  
		Last Modified: Sun, 29 Dec 2019 06:30:56 GMT  
		Size: 23.1 MB (23111296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157f5ff977a61a4741a6f29526e7e2704ab8fa4dbfd0a2f9d0b91d12e6310e82`  
		Last Modified: Sun, 29 Dec 2019 06:30:52 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d0332bc8709680545a1c948edb00d8997c586be0c98ca6555046bfbf9db8e1`  
		Last Modified: Sun, 29 Dec 2019 06:30:53 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:1.7-meta-alpine`

```console
$ docker pull influxdb@sha256:2698eb235a7d511806afa90170f36042daf1c1781f23d17d0477146290fd1680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:1.7-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:55e3a53d0a1f916d645e9d6b2e836ae52f9e022e58f0140b611c286f1841fc35
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27667539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71940ce7e5292095e4b97298e83867f126f12866aacb7041faeef5c873ec2068`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:05:40 GMT
ENV INFLUXDB_VERSION=1.7.9-c1.7.9
# Thu, 23 Jan 2020 19:06:15 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:06:15 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 23 Jan 2020 19:06:16 GMT
EXPOSE 8091
# Thu, 23 Jan 2020 19:06:16 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:06:16 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:06:17 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1201b89c275e51d5ea3297ef0f864075cf880dc9657b2aac87262b1dfb0cd9`  
		Last Modified: Thu, 23 Jan 2020 19:10:29 GMT  
		Size: 23.0 MB (23038963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831486b4a2e07cc7b242a6ca828ff04a4b237d93d23dc31a05fe171693fa8601`  
		Last Modified: Thu, 23 Jan 2020 19:10:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436b73eccb9dcbcc4d58635426554f6addfcbfd851e641e76ea351593e07526f`  
		Last Modified: Thu, 23 Jan 2020 19:10:16 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:a881bfd6d054ae96e0a9669da1b38c70144b443c2480b195328c8751b07435a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:bc7547720eb71080dafbe914948fe69e3e54af7d213720742b004b8734597ed3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68514959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d066753d5076f97093b0413b3af936ca251ed6317ed4b8e825e111e3ddcad7b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:05:18 GMT
ENV INFLUXDB_VERSION=1.7.9
# Thu, 23 Jan 2020 19:05:29 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:05:30 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:05:30 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:05:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:05:30 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:05:31 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:05:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:05:31 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d218467912abf62e1cd393acb1624443c7ff3172f0a6af7ea7305f08299428`  
		Last Modified: Thu, 23 Jan 2020 19:09:15 GMT  
		Size: 63.9 MB (63885240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12383a31bf0090401b7b255d852b9933d2efbae1d71266f6b6ae1282601edd09`  
		Last Modified: Thu, 23 Jan 2020 19:08:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2e6e59d80a3f4b471e33b68df37295b7f67cf72d977c9465296728721f1386`  
		Last Modified: Thu, 23 Jan 2020 19:08:38 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40749feb0df7c4bbc95d63eb2303aef3ffaeb51982dbd03306056fda86826656`  
		Last Modified: Thu, 23 Jan 2020 19:08:38 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data`

```console
$ docker pull influxdb@sha256:4ddf5fb7da3f7246e48703507a52fac709cae4991adedad52f81e1af7900333e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:57cdf9a41cd906ac2310c973d7148e99c51e7980f6bd4d86e538132ebb5da668
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148393207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a615427926c193674d5b91ce77c1dc37bdbcc365b88f754df1f551e27f0ad62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:28:49 GMT
ENV INFLUXDB_VERSION=1.7.9-c1.7.9
# Sun, 29 Dec 2019 06:28:58 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Sun, 29 Dec 2019 06:28:59 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Sun, 29 Dec 2019 06:28:59 GMT
EXPOSE 8086
# Sun, 29 Dec 2019 06:28:59 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:28:59 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:28:59 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 29 Dec 2019 06:29:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:29:00 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1664952a037d5402a4308e43a84fb2c5bacd6db6d56fa62c4a6083884030d181`  
		Last Modified: Sun, 29 Dec 2019 06:30:48 GMT  
		Size: 87.9 MB (87870575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f41c229695736d78455e0ff175d3e008c640e243384a4b0f71237b94510de3`  
		Last Modified: Sun, 29 Dec 2019 06:30:35 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10245fe741944c997011e2eb9e1e05214057716b71779347c79f32926c9b075`  
		Last Modified: Sun, 29 Dec 2019 06:30:35 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a8bde191a956fadeedc4b8086eb2f3ce254f938d9a30faafd99ba22336c276`  
		Last Modified: Sun, 29 Dec 2019 06:30:35 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:f0dd6bb327087a283c78b7e65f7e93e0b4f9838188e95272dd4d7cd99aa0b0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:aef6f1a0b2f9bd78cf6f829731067f0c1473debf2704adf0a100dfe39353a45d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92253550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01619e7ca41394223b57f6e234b259438bb55f2cd7895deb08c0e7ae2bdccb4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:05:40 GMT
ENV INFLUXDB_VERSION=1.7.9-c1.7.9
# Thu, 23 Jan 2020 19:05:56 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:05:56 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Thu, 23 Jan 2020 19:05:56 GMT
EXPOSE 8086
# Thu, 23 Jan 2020 19:05:57 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:05:57 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:05:57 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Thu, 23 Jan 2020 19:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:05:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945860f7f362c3f0c4ca173502f7357f4bd11da518e63157172d962cac202822`  
		Last Modified: Thu, 23 Jan 2020 19:10:09 GMT  
		Size: 87.6 MB (87623773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48d098bf00bf9fd66c31ac5573d78e18d818f2af4e1fd23963b6afd87e8aba5`  
		Last Modified: Thu, 23 Jan 2020 19:09:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5af9859c16f3d3b8f91016c0943ddbd4f6251c8e2a7880d368793925939338`  
		Last Modified: Thu, 23 Jan 2020 19:09:22 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448822405007cb2b61d086e1995ba31ce9961ef4c913e466603666d2e4a524d8`  
		Last Modified: Thu, 23 Jan 2020 19:09:21 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:ffebb633e8687bbbf532fdaae15b77eede76c9c648a5be1ecb03b399c179c488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:13f33ed5731bf1c367af2883da07ee221b3d824defd197bdfd08ceb5b6fe89fe
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124601200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30239b6d566444bce9e784d219b7bcf1d5bce1afae9f2415ffce9e14cc181433`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:28:32 GMT
ENV INFLUXDB_VERSION=1.7.9
# Sun, 29 Dec 2019 06:28:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sun, 29 Dec 2019 06:28:40 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sun, 29 Dec 2019 06:28:40 GMT
EXPOSE 8086
# Sun, 29 Dec 2019 06:28:40 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:28:40 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:28:40 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 29 Dec 2019 06:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:28:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750868d0ab2b42433705cc20081242d05642ffade36624525f71c57c396ce4d5`  
		Last Modified: Sun, 29 Dec 2019 06:30:30 GMT  
		Size: 64.1 MB (64078627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d98645d729ddaed0c07fa36d92cf3d3a8ba23f0f4adcf3afa569fa6211a1e7`  
		Last Modified: Sun, 29 Dec 2019 06:30:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bd5f153b8d6f3db65f0966dfeaeb3665658bc071c424416c01de6c6e4ea12e`  
		Last Modified: Sun, 29 Dec 2019 06:30:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f458001f5cb1d481787a16c62de8411e5f8e79d6f40abffe37cfc92677551283`  
		Last Modified: Sun, 29 Dec 2019 06:30:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm variant v7

```console
$ docker pull influxdb@sha256:6f3d5a4206e067c6044bbe3cb2ef5d257e2a4e1a7e2a1d5f1c96b86edcd3c529
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116153019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9386ab7cb9ca9f58a1e20e72fa561de761d7444b1b04f6518bbb841ab89a0a16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:19 GMT
ADD file:5692a55e4805d33baa21e559cc0bb86fb91422171345ddd332fa5514285a3401 in / 
# Sat, 28 Dec 2019 05:03:25 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:59:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:00:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 22:31:12 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 28 Dec 2019 22:32:16 GMT
ENV INFLUXDB_VERSION=1.7.9
# Sat, 28 Dec 2019 22:32:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sat, 28 Dec 2019 22:32:32 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sat, 28 Dec 2019 22:32:33 GMT
EXPOSE 8086
# Sat, 28 Dec 2019 22:32:34 GMT
VOLUME [/var/lib/influxdb]
# Sat, 28 Dec 2019 22:32:35 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sat, 28 Dec 2019 22:32:36 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sat, 28 Dec 2019 22:32:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 22:32:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:b531ae4a39253d883a11291e842b7e1aa9dae38f9d9b77ddea55b2625ce986e3`  
		Last Modified: Sat, 28 Dec 2019 05:10:53 GMT  
		Size: 42.1 MB (42108124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22754f6fc5d5a244119c0928ebf7d851d276d7f095f07e6bf435fa7afbcab8a8`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 9.5 MB (9498197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2155e4b3456accbea4b6873247312dd288feb477ec966ed48637e031aba558`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 3.9 MB (3918728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74fbc8f56f35aa5563c51e2a9dca9b6899524e044502d812a7ba6647e9449af`  
		Last Modified: Sat, 28 Dec 2019 22:32:52 GMT  
		Size: 2.8 KB (2802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80159293deebc34af54888faedc28abd12bf3071eb269dd8b7dff608338e3de5`  
		Last Modified: Sat, 28 Dec 2019 22:33:38 GMT  
		Size: 60.6 MB (60623453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2646782f025a8df2d3843af35f5056f1ce1f09bc95b1d4cb0e1aab30b4fcab6`  
		Last Modified: Sat, 28 Dec 2019 22:33:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf200223c03eedf7cde1432a96d6fe4fc0bf00fdcd3cd310c2843bb1beb23bdb`  
		Last Modified: Sat, 28 Dec 2019 22:33:22 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7bf79b2957e32b043378643aee8ec72e2d50573519c94335e2182429a923a6`  
		Last Modified: Sat, 28 Dec 2019 22:33:22 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:08fcd09b2f430d8f49e5cc1ec33b8e11120688d421d2715f037974f81a538a20
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117132805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f0618279fcd0fadb8b20ce70b686bbed61b23e5ed8f56a08147bf1f6b655fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:01 GMT
ADD file:1618e6474dbe6462a610ce7eed99f0bfd087ea37ddfc287bbd69def5c24ede47 in / 
# Sat, 01 Feb 2020 16:43:02 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:29:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 02 Feb 2020 11:06:15 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 02 Feb 2020 11:06:48 GMT
ENV INFLUXDB_VERSION=1.7.9
# Sun, 02 Feb 2020 11:06:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_${ARCH}.deb.asc influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_${ARCH}.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_${ARCH}.deb*
# Sun, 02 Feb 2020 11:06:58 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Sun, 02 Feb 2020 11:06:59 GMT
EXPOSE 8086
# Sun, 02 Feb 2020 11:06:59 GMT
VOLUME [/var/lib/influxdb]
# Sun, 02 Feb 2020 11:07:00 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Sun, 02 Feb 2020 11:07:00 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Sun, 02 Feb 2020 11:07:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 11:07:02 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:df3de44c7096ba135556a1e7044f9e1feee3ef713ab96f0416f71fe78422cbf6`  
		Last Modified: Sat, 01 Feb 2020 16:48:40 GMT  
		Size: 43.2 MB (43166749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf173a01baf7d45b479bb380ece219cbf0ea52178e9b8cdc5b87891759d1122`  
		Last Modified: Sat, 01 Feb 2020 17:39:19 GMT  
		Size: 9.7 MB (9748586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3392eac7bc27f3bd5fcb024413ca55ec4115c22da3e229567d5fc03cd4ff4e4`  
		Last Modified: Sat, 01 Feb 2020 17:39:18 GMT  
		Size: 4.1 MB (4094322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde65a8145ef90dfe307279a53df204fa49964b14b50014ede6314e6cfb19397`  
		Last Modified: Sun, 02 Feb 2020 11:07:12 GMT  
		Size: 2.8 KB (2804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a768f38cf9405d857c8a5ef871661c9e7c4d4d9199da3284adea507adb89d59`  
		Last Modified: Sun, 02 Feb 2020 11:07:54 GMT  
		Size: 60.1 MB (60118628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5d4130725ae5650df1a864df1dbc0e79dd427c0f8fdeabc0dd8aafe0e9930a`  
		Last Modified: Sun, 02 Feb 2020 11:07:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee4f315db6d4214c07e621be52a57fb91c7ceeaf240290d58f36a153816bef8`  
		Last Modified: Sun, 02 Feb 2020 11:07:38 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101a642eb058840e738465178e38eeb41abc35bcdb9130f6576ee4a035381080`  
		Last Modified: Sun, 02 Feb 2020 11:07:38 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:4a24e768612c7a919f0dbddb7ad0fbe053e851965b24a7721d2e0d7188ee6d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:c29f2fda2fe60adcb728a7f0bb4438cec14b6d4340a8824f82538ac334f2474a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83632722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc55042149f8c769f4a4d0dff3fdc7af04c1c4ecd5d997d66f1947a83ad04ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 Dec 2019 06:27:21 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 29 Dec 2019 06:28:49 GMT
ENV INFLUXDB_VERSION=1.7.9-c1.7.9
# Sun, 29 Dec 2019 06:29:11 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Sun, 29 Dec 2019 06:29:11 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Sun, 29 Dec 2019 06:29:11 GMT
EXPOSE 8091
# Sun, 29 Dec 2019 06:29:11 GMT
VOLUME [/var/lib/influxdb]
# Sun, 29 Dec 2019 06:29:11 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Sun, 29 Dec 2019 06:29:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 29 Dec 2019 06:29:12 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd32e36b4889f97a22dd58208b310c6935606f3429d48d1349137fd1847aff9`  
		Last Modified: Sun, 29 Dec 2019 06:29:31 GMT  
		Size: 2.8 KB (2777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959e4fc8e7e5f1e5ab8933a44756baca38d03367fcb64ce390ac5bfda728593d`  
		Last Modified: Sun, 29 Dec 2019 06:30:56 GMT  
		Size: 23.1 MB (23111296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157f5ff977a61a4741a6f29526e7e2704ab8fa4dbfd0a2f9d0b91d12e6310e82`  
		Last Modified: Sun, 29 Dec 2019 06:30:52 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d0332bc8709680545a1c948edb00d8997c586be0c98ca6555046bfbf9db8e1`  
		Last Modified: Sun, 29 Dec 2019 06:30:53 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:2698eb235a7d511806afa90170f36042daf1c1781f23d17d0477146290fd1680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:55e3a53d0a1f916d645e9d6b2e836ae52f9e022e58f0140b611c286f1841fc35
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27667539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71940ce7e5292095e4b97298e83867f126f12866aacb7041faeef5c873ec2068`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:03:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Thu, 23 Jan 2020 19:05:40 GMT
ENV INFLUXDB_VERSION=1.7.9-c1.7.9
# Thu, 23 Jan 2020 19:06:15 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 23 Jan 2020 19:06:15 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Thu, 23 Jan 2020 19:06:16 GMT
EXPOSE 8091
# Thu, 23 Jan 2020 19:06:16 GMT
VOLUME [/var/lib/influxdb]
# Thu, 23 Jan 2020 19:06:16 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Thu, 23 Jan 2020 19:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 19:06:17 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ba98451b59ee73b35b91872f93cee8f4ac91f7488907e033b4db88fdb4074`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 1.9 MB (1863680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1201b89c275e51d5ea3297ef0f864075cf880dc9657b2aac87262b1dfb0cd9`  
		Last Modified: Thu, 23 Jan 2020 19:10:29 GMT  
		Size: 23.0 MB (23038963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831486b4a2e07cc7b242a6ca828ff04a4b237d93d23dc31a05fe171693fa8601`  
		Last Modified: Thu, 23 Jan 2020 19:10:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436b73eccb9dcbcc4d58635426554f6addfcbfd851e641e76ea351593e07526f`  
		Last Modified: Thu, 23 Jan 2020 19:10:16 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
