<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.5`](#kapacitor15)
-	[`kapacitor:1.5-alpine`](#kapacitor15-alpine)
-	[`kapacitor:1.5.9`](#kapacitor159)
-	[`kapacitor:1.5.9-alpine`](#kapacitor159-alpine)
-	[`kapacitor:1.6`](#kapacitor16)
-	[`kapacitor:1.6-alpine`](#kapacitor16-alpine)
-	[`kapacitor:1.6.5`](#kapacitor165)
-	[`kapacitor:1.6.5-alpine`](#kapacitor165-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.5`

```console
$ docker pull kapacitor@sha256:f15d356c56807b8ab090f6b552d6ccc3f8c1c79dc47f842fa2ffc23493032ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:d69918dde8206b8093ebf4232f85cd3e2cf38db0f848b26e6005bb932a667011
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111735184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc00b6e833611385f4ceb08786c82eb15567465e1a82839a32e1f010206afe22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:10 GMT
ADD file:4c5e0bec5f780d9c6bfbafcb9e6ed641781dd7f7c2853a0c49d6613e9fef9516 in / 
# Thu, 23 Jun 2022 00:22:10 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:54:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:54:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 15:23:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 23 Jun 2022 15:23:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 15:23:16 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 23 Jun 2022 15:23:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 23 Jun 2022 15:23:21 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 23 Jun 2022 15:23:21 GMT
EXPOSE 9092
# Thu, 23 Jun 2022 15:23:22 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 23 Jun 2022 15:23:22 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 23 Jun 2022 15:23:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 15:23:22 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:8372a04f222be82bf67eb0010a59644b1e52f1246b3da9034edaa98f3d591cae`  
		Last Modified: Thu, 23 Jun 2022 00:29:36 GMT  
		Size: 45.4 MB (45430020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1728fee80d376293a9ef5fdcc0acd3f6398fc4159b12064ce4c1e66f67e7e9d`  
		Last Modified: Thu, 23 Jun 2022 01:02:01 GMT  
		Size: 11.3 MB (11302923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cf50aa0a4b80b39d1bf4be232d404da0b1ad38cdd3bb1a017b727947b5f4bb`  
		Last Modified: Thu, 23 Jun 2022 01:02:00 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ca30eaa3f2e4a14053445907d290c9e29fe087a4cd7f7607ea7ced493a2405`  
		Last Modified: Thu, 23 Jun 2022 15:23:51 GMT  
		Size: 13.4 MB (13436157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88da6edad4b4d98978e4fd397110c9d2f14f317fd3846dc196f8d8c95d1ba632`  
		Last Modified: Thu, 23 Jun 2022 15:23:50 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eb7eb8e6acbbca57e804e463d57e0e255e32445eeaaddc76c8e5a910ee927e`  
		Last Modified: Thu, 23 Jun 2022 15:23:54 GMT  
		Size: 37.2 MB (37219849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed57900e7789f09136c4dbf3c3848e6f4ddf2d4cc4d75afe52c633a40c72470`  
		Last Modified: Thu, 23 Jun 2022 15:23:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a2e325e760c8c507dfb8d86f51accfe003b032a99742ef67b8816a676277c6`  
		Last Modified: Thu, 23 Jun 2022 15:23:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:cd9f3dc09aa94337e69fe1d38c3a5b5b007eec7ec6376223c85672f0a8020bf0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104444329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ddd6754fe6eb13a51d001f3cb565f193c0ff966b8033dbdc6d926187284f1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 23 Jun 2022 01:05:04 GMT
ADD file:4f45aa06c6a1c011e41ff7e4685f05d91970973768fc88ff3e825c5ac4fd6058 in / 
# Thu, 23 Jun 2022 01:05:05 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:58:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 25 Aug 2022 13:33:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 25 Aug 2022 13:33:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 25 Aug 2022 13:33:43 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 25 Aug 2022 13:33:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 25 Aug 2022 13:33:49 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 25 Aug 2022 13:33:49 GMT
EXPOSE 9092
# Thu, 25 Aug 2022 13:33:50 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 25 Aug 2022 13:33:50 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 25 Aug 2022 13:33:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Aug 2022 13:33:50 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:cf35481e5c316d184dac1873898948d1e8108de590a2a940c32cda34173fe7c1`  
		Last Modified: Thu, 23 Jun 2022 01:22:04 GMT  
		Size: 42.2 MB (42150850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b740b174e94fb77095522004355bb6f430f0b25308acd5fc66d325f04f99c6`  
		Last Modified: Thu, 23 Jun 2022 02:21:27 GMT  
		Size: 10.0 MB (9957097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf98bd2fdfbc26a0f8c12d47c32e612d01389ff5e4aafc52aa04b72381a6c823`  
		Last Modified: Thu, 23 Jun 2022 02:21:24 GMT  
		Size: 3.9 MB (3921761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fdb374fea931096d12384c28514fb299f3757bb79db739f2f59d801e6d88aa`  
		Last Modified: Thu, 25 Aug 2022 13:34:07 GMT  
		Size: 13.6 MB (13624240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4d4ae23752184f4e684dd83e2afb54d03d52918fb6a4f072f011e87d167c3b`  
		Last Modified: Thu, 25 Aug 2022 13:34:05 GMT  
		Size: 2.9 KB (2859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad709a6376d8b6eca573d0aa724ab46ff7c35626f6614fbd73ddd69437b99fe9`  
		Last Modified: Thu, 25 Aug 2022 13:34:11 GMT  
		Size: 34.8 MB (34787066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0965ac7524ab0bbf5f0f4c66a9d58995cf7382d552d904d081a9a598b08aa895`  
		Last Modified: Thu, 25 Aug 2022 13:34:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aaf5bcc8e4fc72bfbb26732670fab742777af27c29c7062f41cc96494452258`  
		Last Modified: Thu, 25 Aug 2022 13:34:04 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:d64ca5380929ee7878f5e8306bba8daf8decce31947206e47f9659fb0932e032
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104787715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b332039c83beb1f9eb398bc82dd619070c5a1f91a6b8780ea2ea27c2497d3aee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:45 GMT
ADD file:3d8b1da94fcec5d068e3e6465fac70cce404c331bb52e30a5bf7cbd950baa5fe in / 
# Thu, 23 Jun 2022 00:42:45 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:15:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:16:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 19:53:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 23 Jun 2022 19:53:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 19:53:26 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 23 Jun 2022 19:53:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 23 Jun 2022 19:53:33 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 23 Jun 2022 19:53:33 GMT
EXPOSE 9092
# Thu, 23 Jun 2022 19:53:34 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 23 Jun 2022 19:53:36 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 23 Jun 2022 19:53:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 19:53:37 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d8ccec8a513f896fedd1d9765f3f2abf98bc8264f61cecf17919c80c9aa7ddbc`  
		Last Modified: Thu, 23 Jun 2022 00:51:18 GMT  
		Size: 43.2 MB (43213121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b40625a6bb21cb2cd6b19ef7592951f90da9ea1d8abf359196bf48300c448b2`  
		Last Modified: Thu, 23 Jun 2022 01:25:28 GMT  
		Size: 10.2 MB (10218617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414226169d0f92fdcd77314cbd06ba7613675d62a3afd63aa88afbf0072c44c2`  
		Last Modified: Thu, 23 Jun 2022 01:25:27 GMT  
		Size: 3.9 MB (3874558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8542c55f48f306c6a90e1aa6f29055312f14b902314a5ca9c68892c322de92ed`  
		Last Modified: Thu, 23 Jun 2022 19:54:14 GMT  
		Size: 12.9 MB (12917403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446cc2e960cab2a956d4d3e32ebeed4499cc4d1510c77d1bacfe25a2c8c17cb2`  
		Last Modified: Thu, 23 Jun 2022 19:54:13 GMT  
		Size: 2.8 KB (2823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c624dee0b468a9291c6553c68a74e861f562ad6d4f4f09ec9342e9db71c69f`  
		Last Modified: Thu, 23 Jun 2022 19:54:17 GMT  
		Size: 34.6 MB (34560739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40b4c538f7c74a41a1511239e5d02a39b7200049a92666adcd598e163f70103`  
		Last Modified: Thu, 23 Jun 2022 19:54:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b217b4b3a6c0cac3b49e459fcfde5c541fadc33ccaa199887246bf425414bd`  
		Last Modified: Thu, 23 Jun 2022 19:54:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5-alpine`

```console
$ docker pull kapacitor@sha256:f0f31429af6264e22af1e8775ee4f5b068f8c252dbb12a18dc7ca8bca6021e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:19babd50485107fc60c68c5575e10fcfcaab84a061f1f8d33c8777f89a83f67e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22653543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4c0dc3fc30734367b70939eab1f65f2b9415e94acb5a2a30ddbcd7cd9ff4a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:15:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 06 Oct 2022 20:15:37 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 06 Oct 2022 22:59:26 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 06 Oct 2022 22:59:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 06 Oct 2022 22:59:32 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 06 Oct 2022 22:59:32 GMT
EXPOSE 9092
# Thu, 06 Oct 2022 22:59:32 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 06 Oct 2022 22:59:32 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 06 Oct 2022 22:59:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 22:59:32 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133509570f70da73b5369d8311a4269568dbea851313f10ea1b8cb1a2c4e2fe8`  
		Last Modified: Thu, 06 Oct 2022 20:16:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed07ae854e5b9e7d93d0c5eb8bbcfb2d6e5eddeb00720efe7b55766ce5bfbab`  
		Last Modified: Thu, 06 Oct 2022 20:16:41 GMT  
		Size: 284.6 KB (284583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ae6d710af90b1b33cb522971dfe089e2211f3ab1ca3fd49c413a6abb65bca3`  
		Last Modified: Thu, 06 Oct 2022 23:00:14 GMT  
		Size: 19.5 MB (19540837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824abcf1a6f5277dc3c036fcbd7fd7fe396a7e46833634600dd503e0dbb06cff`  
		Last Modified: Thu, 06 Oct 2022 23:00:11 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b85cbf909734bf9f5784fa910bb4cd8b7b1dd2121001a8a1a34362ba54ae46e`  
		Last Modified: Thu, 06 Oct 2022 23:00:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.9`

```console
$ docker pull kapacitor@sha256:f15d356c56807b8ab090f6b552d6ccc3f8c1c79dc47f842fa2ffc23493032ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5.9` - linux; amd64

```console
$ docker pull kapacitor@sha256:d69918dde8206b8093ebf4232f85cd3e2cf38db0f848b26e6005bb932a667011
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111735184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc00b6e833611385f4ceb08786c82eb15567465e1a82839a32e1f010206afe22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 23 Jun 2022 00:22:10 GMT
ADD file:4c5e0bec5f780d9c6bfbafcb9e6ed641781dd7f7c2853a0c49d6613e9fef9516 in / 
# Thu, 23 Jun 2022 00:22:10 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:54:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:54:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 15:23:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 23 Jun 2022 15:23:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 15:23:16 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 23 Jun 2022 15:23:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 23 Jun 2022 15:23:21 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 23 Jun 2022 15:23:21 GMT
EXPOSE 9092
# Thu, 23 Jun 2022 15:23:22 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 23 Jun 2022 15:23:22 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 23 Jun 2022 15:23:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 15:23:22 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:8372a04f222be82bf67eb0010a59644b1e52f1246b3da9034edaa98f3d591cae`  
		Last Modified: Thu, 23 Jun 2022 00:29:36 GMT  
		Size: 45.4 MB (45430020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1728fee80d376293a9ef5fdcc0acd3f6398fc4159b12064ce4c1e66f67e7e9d`  
		Last Modified: Thu, 23 Jun 2022 01:02:01 GMT  
		Size: 11.3 MB (11302923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cf50aa0a4b80b39d1bf4be232d404da0b1ad38cdd3bb1a017b727947b5f4bb`  
		Last Modified: Thu, 23 Jun 2022 01:02:00 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ca30eaa3f2e4a14053445907d290c9e29fe087a4cd7f7607ea7ced493a2405`  
		Last Modified: Thu, 23 Jun 2022 15:23:51 GMT  
		Size: 13.4 MB (13436157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88da6edad4b4d98978e4fd397110c9d2f14f317fd3846dc196f8d8c95d1ba632`  
		Last Modified: Thu, 23 Jun 2022 15:23:50 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eb7eb8e6acbbca57e804e463d57e0e255e32445eeaaddc76c8e5a910ee927e`  
		Last Modified: Thu, 23 Jun 2022 15:23:54 GMT  
		Size: 37.2 MB (37219849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed57900e7789f09136c4dbf3c3848e6f4ddf2d4cc4d75afe52c633a40c72470`  
		Last Modified: Thu, 23 Jun 2022 15:23:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a2e325e760c8c507dfb8d86f51accfe003b032a99742ef67b8816a676277c6`  
		Last Modified: Thu, 23 Jun 2022 15:23:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.9` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:cd9f3dc09aa94337e69fe1d38c3a5b5b007eec7ec6376223c85672f0a8020bf0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104444329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ddd6754fe6eb13a51d001f3cb565f193c0ff966b8033dbdc6d926187284f1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 23 Jun 2022 01:05:04 GMT
ADD file:4f45aa06c6a1c011e41ff7e4685f05d91970973768fc88ff3e825c5ac4fd6058 in / 
# Thu, 23 Jun 2022 01:05:05 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:58:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 25 Aug 2022 13:33:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 25 Aug 2022 13:33:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 25 Aug 2022 13:33:43 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 25 Aug 2022 13:33:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 25 Aug 2022 13:33:49 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 25 Aug 2022 13:33:49 GMT
EXPOSE 9092
# Thu, 25 Aug 2022 13:33:50 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 25 Aug 2022 13:33:50 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 25 Aug 2022 13:33:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Aug 2022 13:33:50 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:cf35481e5c316d184dac1873898948d1e8108de590a2a940c32cda34173fe7c1`  
		Last Modified: Thu, 23 Jun 2022 01:22:04 GMT  
		Size: 42.2 MB (42150850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b740b174e94fb77095522004355bb6f430f0b25308acd5fc66d325f04f99c6`  
		Last Modified: Thu, 23 Jun 2022 02:21:27 GMT  
		Size: 10.0 MB (9957097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf98bd2fdfbc26a0f8c12d47c32e612d01389ff5e4aafc52aa04b72381a6c823`  
		Last Modified: Thu, 23 Jun 2022 02:21:24 GMT  
		Size: 3.9 MB (3921761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fdb374fea931096d12384c28514fb299f3757bb79db739f2f59d801e6d88aa`  
		Last Modified: Thu, 25 Aug 2022 13:34:07 GMT  
		Size: 13.6 MB (13624240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4d4ae23752184f4e684dd83e2afb54d03d52918fb6a4f072f011e87d167c3b`  
		Last Modified: Thu, 25 Aug 2022 13:34:05 GMT  
		Size: 2.9 KB (2859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad709a6376d8b6eca573d0aa724ab46ff7c35626f6614fbd73ddd69437b99fe9`  
		Last Modified: Thu, 25 Aug 2022 13:34:11 GMT  
		Size: 34.8 MB (34787066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0965ac7524ab0bbf5f0f4c66a9d58995cf7382d552d904d081a9a598b08aa895`  
		Last Modified: Thu, 25 Aug 2022 13:34:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aaf5bcc8e4fc72bfbb26732670fab742777af27c29c7062f41cc96494452258`  
		Last Modified: Thu, 25 Aug 2022 13:34:04 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.9` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:d64ca5380929ee7878f5e8306bba8daf8decce31947206e47f9659fb0932e032
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104787715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b332039c83beb1f9eb398bc82dd619070c5a1f91a6b8780ea2ea27c2497d3aee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:45 GMT
ADD file:3d8b1da94fcec5d068e3e6465fac70cce404c331bb52e30a5bf7cbd950baa5fe in / 
# Thu, 23 Jun 2022 00:42:45 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:15:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:16:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 19:53:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 23 Jun 2022 19:53:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Jun 2022 19:53:26 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 23 Jun 2022 19:53:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 23 Jun 2022 19:53:33 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 23 Jun 2022 19:53:33 GMT
EXPOSE 9092
# Thu, 23 Jun 2022 19:53:34 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 23 Jun 2022 19:53:36 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 23 Jun 2022 19:53:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 19:53:37 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d8ccec8a513f896fedd1d9765f3f2abf98bc8264f61cecf17919c80c9aa7ddbc`  
		Last Modified: Thu, 23 Jun 2022 00:51:18 GMT  
		Size: 43.2 MB (43213121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b40625a6bb21cb2cd6b19ef7592951f90da9ea1d8abf359196bf48300c448b2`  
		Last Modified: Thu, 23 Jun 2022 01:25:28 GMT  
		Size: 10.2 MB (10218617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414226169d0f92fdcd77314cbd06ba7613675d62a3afd63aa88afbf0072c44c2`  
		Last Modified: Thu, 23 Jun 2022 01:25:27 GMT  
		Size: 3.9 MB (3874558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8542c55f48f306c6a90e1aa6f29055312f14b902314a5ca9c68892c322de92ed`  
		Last Modified: Thu, 23 Jun 2022 19:54:14 GMT  
		Size: 12.9 MB (12917403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446cc2e960cab2a956d4d3e32ebeed4499cc4d1510c77d1bacfe25a2c8c17cb2`  
		Last Modified: Thu, 23 Jun 2022 19:54:13 GMT  
		Size: 2.8 KB (2823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c624dee0b468a9291c6553c68a74e861f562ad6d4f4f09ec9342e9db71c69f`  
		Last Modified: Thu, 23 Jun 2022 19:54:17 GMT  
		Size: 34.6 MB (34560739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40b4c538f7c74a41a1511239e5d02a39b7200049a92666adcd598e163f70103`  
		Last Modified: Thu, 23 Jun 2022 19:54:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b217b4b3a6c0cac3b49e459fcfde5c541fadc33ccaa199887246bf425414bd`  
		Last Modified: Thu, 23 Jun 2022 19:54:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.9-alpine`

```console
$ docker pull kapacitor@sha256:f0f31429af6264e22af1e8775ee4f5b068f8c252dbb12a18dc7ca8bca6021e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.5.9-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:19babd50485107fc60c68c5575e10fcfcaab84a061f1f8d33c8777f89a83f67e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22653543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4c0dc3fc30734367b70939eab1f65f2b9415e94acb5a2a30ddbcd7cd9ff4a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:15:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 06 Oct 2022 20:15:37 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 06 Oct 2022 22:59:26 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 06 Oct 2022 22:59:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 06 Oct 2022 22:59:32 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 06 Oct 2022 22:59:32 GMT
EXPOSE 9092
# Thu, 06 Oct 2022 22:59:32 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 06 Oct 2022 22:59:32 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 06 Oct 2022 22:59:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 22:59:32 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133509570f70da73b5369d8311a4269568dbea851313f10ea1b8cb1a2c4e2fe8`  
		Last Modified: Thu, 06 Oct 2022 20:16:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed07ae854e5b9e7d93d0c5eb8bbcfb2d6e5eddeb00720efe7b55766ce5bfbab`  
		Last Modified: Thu, 06 Oct 2022 20:16:41 GMT  
		Size: 284.6 KB (284583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ae6d710af90b1b33cb522971dfe089e2211f3ab1ca3fd49c413a6abb65bca3`  
		Last Modified: Thu, 06 Oct 2022 23:00:14 GMT  
		Size: 19.5 MB (19540837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824abcf1a6f5277dc3c036fcbd7fd7fe396a7e46833634600dd503e0dbb06cff`  
		Last Modified: Thu, 06 Oct 2022 23:00:11 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b85cbf909734bf9f5784fa910bb4cd8b7b1dd2121001a8a1a34362ba54ae46e`  
		Last Modified: Thu, 06 Oct 2022 23:00:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6`

```console
$ docker pull kapacitor@sha256:346421a83bbe8cae69bd6ee21ce9ccfe6541bf2e3f48f96a092ea6b3d04854fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:160a8d0a753af4d222ca03f0f9841902405909aa0595a9587f5f95ced9af707d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130621111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2475f729aa5a99907def4f3a177f8bdc47fccf68966bc06d9742a7149e3e6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:37:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:38:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Oct 2022 01:06:43 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 26 Oct 2022 01:06:43 GMT
ENV KAPACITOR_VERSION=1.6.5
# Wed, 26 Oct 2022 01:06:50 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 26 Oct 2022 01:06:51 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 26 Oct 2022 01:06:51 GMT
EXPOSE 9092
# Wed, 26 Oct 2022 01:06:51 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 26 Oct 2022 01:06:51 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 26 Oct 2022 01:06:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Oct 2022 01:06:51 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5960f4cc2f4ee9a7344c315f226d539b57228b7cb255d5792b5269869d8263`  
		Last Modified: Tue, 25 Oct 2022 09:52:55 GMT  
		Size: 3.8 MB (3804701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8611d4a626ec9a284b2add0e552d72e6fd4898799678363fc7c66d6bca0a5a51`  
		Last Modified: Tue, 25 Oct 2022 09:52:55 GMT  
		Size: 3.6 MB (3561144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38d1949b8906539205e2122505ae24b7db814d6e6e02dae6cc7c09971e0e9a3`  
		Last Modified: Wed, 26 Oct 2022 01:07:14 GMT  
		Size: 28.4 MB (28412154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35015fec98695e1bc8ef8aa53010496b8e7bb55f9767af3428b3a55bdca7f2f4`  
		Last Modified: Wed, 26 Oct 2022 01:07:20 GMT  
		Size: 64.4 MB (64416282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4104f69a4845c93d1534b2eaa70fb4ca3616e0beb4610c6e062815150b5749e2`  
		Last Modified: Wed, 26 Oct 2022 01:07:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6515a15028080899738b7615a8cab5d7cec538ff1b6d8aebb1aaac2559c4feae`  
		Last Modified: Wed, 26 Oct 2022 01:07:11 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:910c8052722650a1e7bb598380da5d2f77737ef2e0234012fd12feba0c78a065
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121893084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932d7d9db65c670e82faff3ffa4f0f03ded9881a9c12e4d173151c5fefb4a897`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:31:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:31:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 17:51:14 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 05 Oct 2022 17:51:14 GMT
ENV KAPACITOR_VERSION=1.6.5
# Wed, 05 Oct 2022 17:51:21 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 17:51:22 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 05 Oct 2022 17:51:22 GMT
EXPOSE 9092
# Wed, 05 Oct 2022 17:51:23 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 05 Oct 2022 17:51:25 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 05 Oct 2022 17:51:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 17:51:26 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664e4680d7b30c1a6751735f5f2e99eea49e96adad47b7382c4944ced1c92764`  
		Last Modified: Wed, 05 Oct 2022 00:42:55 GMT  
		Size: 3.8 MB (3776737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd6f597bdec02a1a3fe9903e9fef999621ae074f289e4bf2e8fb5a209f38722`  
		Last Modified: Wed, 05 Oct 2022 00:42:55 GMT  
		Size: 3.3 MB (3320776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b8a48a8516c821779750a2489f7060b47d010e814701b0d46b4be678d39ad6`  
		Last Modified: Wed, 05 Oct 2022 17:51:49 GMT  
		Size: 25.5 MB (25491262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06462dab540ac7e6aa4521b2f22006fc500d7150219a7a2a572ee0422a9ece8`  
		Last Modified: Wed, 05 Oct 2022 17:51:54 GMT  
		Size: 60.9 MB (60921597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddbe132a6ba48a91993062836cf48959c351bd479810e128aec08dc3f9651f8`  
		Last Modified: Wed, 05 Oct 2022 17:51:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a974a9f23b7f0d9fc1a8ab9c591ebb4c8fe77338c06bfddb33b30037a8a952d`  
		Last Modified: Wed, 05 Oct 2022 17:51:47 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6-alpine`

```console
$ docker pull kapacitor@sha256:f2d77c86a9680f182d016c5eef51dcd039cd59a1f2dee8f1cc6b3e957519a812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e27445333bd7864ded5eba8f62c29e860e39bf6794201899c8b980587c676691
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67432365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6b500e445a620ee787bbfcdb314860d5713e0793b51a8cd8c1cc4b0dcaa562`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:59:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 06 Oct 2022 22:59:38 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 06 Oct 2022 22:59:38 GMT
ENV KAPACITOR_VERSION=1.6.5
# Thu, 06 Oct 2022 22:59:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 06 Oct 2022 22:59:51 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 06 Oct 2022 22:59:51 GMT
EXPOSE 9092
# Thu, 06 Oct 2022 22:59:51 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 06 Oct 2022 22:59:51 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 06 Oct 2022 22:59:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 22:59:51 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d30442cf8411e7f53657b11f2e08ef81065f359c49d13af3d255eb9ce50bd8`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91274948dd8749eb88a1567b409dd579615c0d678f7154f95f15ddd03222163c`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 284.7 KB (284738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6038b15547c18f4ea2106297dda7195c2b4c68475ccc5765d20eb45abf50fc`  
		Last Modified: Thu, 06 Oct 2022 23:00:32 GMT  
		Size: 64.3 MB (64340964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2054ab7ab071cb17595fc05391099ad825cb1cb7a486d8594f8f3014fb0758e8`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cf528e02578aa4e995f00e5ea98eb572d949fb4748318ea2d11b15d6a3b28d`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6.5`

```console
$ docker pull kapacitor@sha256:346421a83bbe8cae69bd6ee21ce9ccfe6541bf2e3f48f96a092ea6b3d04854fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:160a8d0a753af4d222ca03f0f9841902405909aa0595a9587f5f95ced9af707d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130621111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2475f729aa5a99907def4f3a177f8bdc47fccf68966bc06d9742a7149e3e6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:37:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:38:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Oct 2022 01:06:43 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 26 Oct 2022 01:06:43 GMT
ENV KAPACITOR_VERSION=1.6.5
# Wed, 26 Oct 2022 01:06:50 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 26 Oct 2022 01:06:51 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 26 Oct 2022 01:06:51 GMT
EXPOSE 9092
# Wed, 26 Oct 2022 01:06:51 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 26 Oct 2022 01:06:51 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 26 Oct 2022 01:06:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Oct 2022 01:06:51 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5960f4cc2f4ee9a7344c315f226d539b57228b7cb255d5792b5269869d8263`  
		Last Modified: Tue, 25 Oct 2022 09:52:55 GMT  
		Size: 3.8 MB (3804701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8611d4a626ec9a284b2add0e552d72e6fd4898799678363fc7c66d6bca0a5a51`  
		Last Modified: Tue, 25 Oct 2022 09:52:55 GMT  
		Size: 3.6 MB (3561144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38d1949b8906539205e2122505ae24b7db814d6e6e02dae6cc7c09971e0e9a3`  
		Last Modified: Wed, 26 Oct 2022 01:07:14 GMT  
		Size: 28.4 MB (28412154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35015fec98695e1bc8ef8aa53010496b8e7bb55f9767af3428b3a55bdca7f2f4`  
		Last Modified: Wed, 26 Oct 2022 01:07:20 GMT  
		Size: 64.4 MB (64416282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4104f69a4845c93d1534b2eaa70fb4ca3616e0beb4610c6e062815150b5749e2`  
		Last Modified: Wed, 26 Oct 2022 01:07:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6515a15028080899738b7615a8cab5d7cec538ff1b6d8aebb1aaac2559c4feae`  
		Last Modified: Wed, 26 Oct 2022 01:07:11 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:910c8052722650a1e7bb598380da5d2f77737ef2e0234012fd12feba0c78a065
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121893084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932d7d9db65c670e82faff3ffa4f0f03ded9881a9c12e4d173151c5fefb4a897`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:31:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:31:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 17:51:14 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 05 Oct 2022 17:51:14 GMT
ENV KAPACITOR_VERSION=1.6.5
# Wed, 05 Oct 2022 17:51:21 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 17:51:22 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 05 Oct 2022 17:51:22 GMT
EXPOSE 9092
# Wed, 05 Oct 2022 17:51:23 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 05 Oct 2022 17:51:25 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 05 Oct 2022 17:51:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 17:51:26 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664e4680d7b30c1a6751735f5f2e99eea49e96adad47b7382c4944ced1c92764`  
		Last Modified: Wed, 05 Oct 2022 00:42:55 GMT  
		Size: 3.8 MB (3776737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd6f597bdec02a1a3fe9903e9fef999621ae074f289e4bf2e8fb5a209f38722`  
		Last Modified: Wed, 05 Oct 2022 00:42:55 GMT  
		Size: 3.3 MB (3320776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b8a48a8516c821779750a2489f7060b47d010e814701b0d46b4be678d39ad6`  
		Last Modified: Wed, 05 Oct 2022 17:51:49 GMT  
		Size: 25.5 MB (25491262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06462dab540ac7e6aa4521b2f22006fc500d7150219a7a2a572ee0422a9ece8`  
		Last Modified: Wed, 05 Oct 2022 17:51:54 GMT  
		Size: 60.9 MB (60921597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddbe132a6ba48a91993062836cf48959c351bd479810e128aec08dc3f9651f8`  
		Last Modified: Wed, 05 Oct 2022 17:51:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a974a9f23b7f0d9fc1a8ab9c591ebb4c8fe77338c06bfddb33b30037a8a952d`  
		Last Modified: Wed, 05 Oct 2022 17:51:47 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6.5-alpine`

```console
$ docker pull kapacitor@sha256:f2d77c86a9680f182d016c5eef51dcd039cd59a1f2dee8f1cc6b3e957519a812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.6.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e27445333bd7864ded5eba8f62c29e860e39bf6794201899c8b980587c676691
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67432365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6b500e445a620ee787bbfcdb314860d5713e0793b51a8cd8c1cc4b0dcaa562`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:59:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 06 Oct 2022 22:59:38 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 06 Oct 2022 22:59:38 GMT
ENV KAPACITOR_VERSION=1.6.5
# Thu, 06 Oct 2022 22:59:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 06 Oct 2022 22:59:51 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 06 Oct 2022 22:59:51 GMT
EXPOSE 9092
# Thu, 06 Oct 2022 22:59:51 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 06 Oct 2022 22:59:51 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 06 Oct 2022 22:59:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 22:59:51 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d30442cf8411e7f53657b11f2e08ef81065f359c49d13af3d255eb9ce50bd8`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91274948dd8749eb88a1567b409dd579615c0d678f7154f95f15ddd03222163c`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 284.7 KB (284738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6038b15547c18f4ea2106297dda7195c2b4c68475ccc5765d20eb45abf50fc`  
		Last Modified: Thu, 06 Oct 2022 23:00:32 GMT  
		Size: 64.3 MB (64340964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2054ab7ab071cb17595fc05391099ad825cb1cb7a486d8594f8f3014fb0758e8`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cf528e02578aa4e995f00e5ea98eb572d949fb4748318ea2d11b15d6a3b28d`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:f2d77c86a9680f182d016c5eef51dcd039cd59a1f2dee8f1cc6b3e957519a812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e27445333bd7864ded5eba8f62c29e860e39bf6794201899c8b980587c676691
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67432365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6b500e445a620ee787bbfcdb314860d5713e0793b51a8cd8c1cc4b0dcaa562`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:59:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 06 Oct 2022 22:59:38 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 06 Oct 2022 22:59:38 GMT
ENV KAPACITOR_VERSION=1.6.5
# Thu, 06 Oct 2022 22:59:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 06 Oct 2022 22:59:51 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 06 Oct 2022 22:59:51 GMT
EXPOSE 9092
# Thu, 06 Oct 2022 22:59:51 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 06 Oct 2022 22:59:51 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 06 Oct 2022 22:59:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Oct 2022 22:59:51 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d30442cf8411e7f53657b11f2e08ef81065f359c49d13af3d255eb9ce50bd8`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91274948dd8749eb88a1567b409dd579615c0d678f7154f95f15ddd03222163c`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 284.7 KB (284738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6038b15547c18f4ea2106297dda7195c2b4c68475ccc5765d20eb45abf50fc`  
		Last Modified: Thu, 06 Oct 2022 23:00:32 GMT  
		Size: 64.3 MB (64340964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2054ab7ab071cb17595fc05391099ad825cb1cb7a486d8594f8f3014fb0758e8`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cf528e02578aa4e995f00e5ea98eb572d949fb4748318ea2d11b15d6a3b28d`  
		Last Modified: Thu, 06 Oct 2022 23:00:25 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:346421a83bbe8cae69bd6ee21ce9ccfe6541bf2e3f48f96a092ea6b3d04854fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:160a8d0a753af4d222ca03f0f9841902405909aa0595a9587f5f95ced9af707d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130621111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2475f729aa5a99907def4f3a177f8bdc47fccf68966bc06d9742a7149e3e6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:37:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:38:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Oct 2022 01:06:43 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 26 Oct 2022 01:06:43 GMT
ENV KAPACITOR_VERSION=1.6.5
# Wed, 26 Oct 2022 01:06:50 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 26 Oct 2022 01:06:51 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 26 Oct 2022 01:06:51 GMT
EXPOSE 9092
# Wed, 26 Oct 2022 01:06:51 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 26 Oct 2022 01:06:51 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 26 Oct 2022 01:06:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Oct 2022 01:06:51 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5960f4cc2f4ee9a7344c315f226d539b57228b7cb255d5792b5269869d8263`  
		Last Modified: Tue, 25 Oct 2022 09:52:55 GMT  
		Size: 3.8 MB (3804701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8611d4a626ec9a284b2add0e552d72e6fd4898799678363fc7c66d6bca0a5a51`  
		Last Modified: Tue, 25 Oct 2022 09:52:55 GMT  
		Size: 3.6 MB (3561144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38d1949b8906539205e2122505ae24b7db814d6e6e02dae6cc7c09971e0e9a3`  
		Last Modified: Wed, 26 Oct 2022 01:07:14 GMT  
		Size: 28.4 MB (28412154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35015fec98695e1bc8ef8aa53010496b8e7bb55f9767af3428b3a55bdca7f2f4`  
		Last Modified: Wed, 26 Oct 2022 01:07:20 GMT  
		Size: 64.4 MB (64416282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4104f69a4845c93d1534b2eaa70fb4ca3616e0beb4610c6e062815150b5749e2`  
		Last Modified: Wed, 26 Oct 2022 01:07:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6515a15028080899738b7615a8cab5d7cec538ff1b6d8aebb1aaac2559c4feae`  
		Last Modified: Wed, 26 Oct 2022 01:07:11 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:910c8052722650a1e7bb598380da5d2f77737ef2e0234012fd12feba0c78a065
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121893084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932d7d9db65c670e82faff3ffa4f0f03ded9881a9c12e4d173151c5fefb4a897`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:31:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:31:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 17:51:14 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 05 Oct 2022 17:51:14 GMT
ENV KAPACITOR_VERSION=1.6.5
# Wed, 05 Oct 2022 17:51:21 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 05 Oct 2022 17:51:22 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 05 Oct 2022 17:51:22 GMT
EXPOSE 9092
# Wed, 05 Oct 2022 17:51:23 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 05 Oct 2022 17:51:25 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 05 Oct 2022 17:51:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 17:51:26 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664e4680d7b30c1a6751735f5f2e99eea49e96adad47b7382c4944ced1c92764`  
		Last Modified: Wed, 05 Oct 2022 00:42:55 GMT  
		Size: 3.8 MB (3776737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd6f597bdec02a1a3fe9903e9fef999621ae074f289e4bf2e8fb5a209f38722`  
		Last Modified: Wed, 05 Oct 2022 00:42:55 GMT  
		Size: 3.3 MB (3320776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b8a48a8516c821779750a2489f7060b47d010e814701b0d46b4be678d39ad6`  
		Last Modified: Wed, 05 Oct 2022 17:51:49 GMT  
		Size: 25.5 MB (25491262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06462dab540ac7e6aa4521b2f22006fc500d7150219a7a2a572ee0422a9ece8`  
		Last Modified: Wed, 05 Oct 2022 17:51:54 GMT  
		Size: 60.9 MB (60921597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddbe132a6ba48a91993062836cf48959c351bd479810e128aec08dc3f9651f8`  
		Last Modified: Wed, 05 Oct 2022 17:51:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a974a9f23b7f0d9fc1a8ab9c591ebb4c8fe77338c06bfddb33b30037a8a952d`  
		Last Modified: Wed, 05 Oct 2022 17:51:47 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
