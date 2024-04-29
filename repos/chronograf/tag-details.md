<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.4`](#chronograf1104)
-	[`chronograf:1.10.4-alpine`](#chronograf1104-alpine)
-	[`chronograf:1.7`](#chronograf17)
-	[`chronograf:1.7-alpine`](#chronograf17-alpine)
-	[`chronograf:1.7.17`](#chronograf1717)
-	[`chronograf:1.7.17-alpine`](#chronograf1717-alpine)
-	[`chronograf:1.8`](#chronograf18)
-	[`chronograf:1.8-alpine`](#chronograf18-alpine)
-	[`chronograf:1.8.10`](#chronograf1810)
-	[`chronograf:1.8.10-alpine`](#chronograf1810-alpine)
-	[`chronograf:1.9`](#chronograf19)
-	[`chronograf:1.9-alpine`](#chronograf19-alpine)
-	[`chronograf:1.9.4`](#chronograf194)
-	[`chronograf:1.9.4-alpine`](#chronograf194-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.10`

```console
$ docker pull chronograf@sha256:00212cde3ec0e7e03064c97967b652a3ccad715a75272d56b16eeb70414f6152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10` - linux; amd64

```console
$ docker pull chronograf@sha256:392c73fd8092f3be72138161975602b6f411a9231b383ce307a8c53e1b292b87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84462839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df456f2e4a0292d497a44d2682d4e00eeeedaafa6b3464dfb2d8b906f2c87d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:54:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 26 Apr 2024 22:08:10 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 22:08:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 26 Apr 2024 22:08:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 26 Apr 2024 22:08:18 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 26 Apr 2024 22:08:18 GMT
EXPOSE 8888
# Fri, 26 Apr 2024 22:08:18 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 22:08:18 GMT
COPY file:322ec550f2fba037831462da9d81d40f7e6c1c94797662b6e166f5d8d36c5b4e in /entrypoint.sh 
# Fri, 26 Apr 2024 22:08:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 22:08:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f2b6422b4a4d96ef0937dc3f999ca0e9a3d3c511bb569f06dabd00917fb88c`  
		Last Modified: Wed, 24 Apr 2024 07:55:22 GMT  
		Size: 7.9 MB (7873309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd8036513aebcbc1aa0503e1eea934239be55bfba53a905f7e2f330f3eb098b`  
		Last Modified: Fri, 26 Apr 2024 22:09:00 GMT  
		Size: 47.4 MB (47414583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898f59b0daa71b77057c779cd4332f4f21f234f0a7f4d7fb396f0c80607788fa`  
		Last Modified: Fri, 26 Apr 2024 22:08:54 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8dc3abe6e300121116e074d1f11f2ac81cbca3b64b2ada8d39bad1ad88fa3a`  
		Last Modified: Fri, 26 Apr 2024 22:08:54 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a177aec86da3c2e057f5f2b64f712e5d1eb9ce89895689ea7009e03de8d2e97`  
		Last Modified: Fri, 26 Apr 2024 22:08:54 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ff93bd9576060dc03a733fd949b2138b6f22a702812151c683edb1b074c63534
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75744378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e27f95eef0625e76a75f07f71d1e2ec121ada9b126ecd4cb001f8d7fa58164`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:48:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 26 Apr 2024 21:59:12 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 21:59:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 26 Apr 2024 21:59:28 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 26 Apr 2024 21:59:28 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 26 Apr 2024 21:59:28 GMT
EXPOSE 8888
# Fri, 26 Apr 2024 21:59:29 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 21:59:29 GMT
COPY file:322ec550f2fba037831462da9d81d40f7e6c1c94797662b6e166f5d8d36c5b4e in /entrypoint.sh 
# Fri, 26 Apr 2024 21:59:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 21:59:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c215aa1ee7dcb414d32d3379d194e0898aeb361148172b49be795e68955e0e6c`  
		Last Modified: Wed, 24 Apr 2024 04:49:20 GMT  
		Size: 6.5 MB (6497997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6652e0b271a4a516ee18f95969d55d8ff1c5e99fab60cd88381e0f92d47df64`  
		Last Modified: Fri, 26 Apr 2024 21:59:55 GMT  
		Size: 44.5 MB (44481468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd921d46385df6c1e4aeb94f04b6a87469a8734325cf5f4f23f14fc5b4fc4d00`  
		Last Modified: Fri, 26 Apr 2024 21:59:46 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8b8a0ecd7b222ce7c45a000b9fae64800ce777eb742cf4ad017ed41c9a6e98`  
		Last Modified: Fri, 26 Apr 2024 21:59:46 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdea724c673507feacd1f1647b5710a94c0962eb15d34b499fb922e402a0f64e`  
		Last Modified: Fri, 26 Apr 2024 21:59:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ef62f8997e8e2908f40073336f7f3ecae0f2d4b873e5eaccf4a0bf1fd0932bfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82039807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e687daa3d3a56538e9daff12e27a705bfbee3f9f1e53f9a0cf30a89b3fb74fcf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 11:12:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 29 Apr 2024 19:59:09 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Mon, 29 Apr 2024 19:59:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 29 Apr 2024 19:59:17 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 29 Apr 2024 19:59:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 29 Apr 2024 19:59:17 GMT
EXPOSE 8888
# Mon, 29 Apr 2024 19:59:17 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Apr 2024 19:59:17 GMT
COPY file:322ec550f2fba037831462da9d81d40f7e6c1c94797662b6e166f5d8d36c5b4e in /entrypoint.sh 
# Mon, 29 Apr 2024 19:59:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Apr 2024 19:59:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3777eaa448d12fa64be79faf0defd5c860f34e6f5785fc5e34b07bd082d784e1`  
		Last Modified: Wed, 24 Apr 2024 11:13:49 GMT  
		Size: 7.6 MB (7649956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9ecf2bddea629649f67d6e6b64ef35f9be939d68ec2fbd9ab4551ac08d0b70`  
		Last Modified: Mon, 29 Apr 2024 19:59:37 GMT  
		Size: 45.2 MB (45185447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b736e8a28ad4ff6c1484f1c6c86899d318f86c8ce53512c3b1e7e9cc7c6cca`  
		Last Modified: Mon, 29 Apr 2024 19:59:31 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66938160c27eb30ea21022ebae3accbc0611e3ec21216bfbb79b93995efb0651`  
		Last Modified: Mon, 29 Apr 2024 19:59:32 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e699ac1e7152c5f174ebd82e9650342f1e2d7a79f4ebfa183934588058b6ebb`  
		Last Modified: Mon, 29 Apr 2024 19:59:31 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:bc677d048b78b7ee3b2339fea88440e7e1e6f36c322adbceaef16bbd4cdd7c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:e4d3d65dfa3b17d25170a680c6e9bb88c2ffc649a7eea1af1b9512d127f61561
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31590092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1aa448b8cb627fb1b3de3e95e85d1792fb7c84a2324e6bacc6cf6f2bd1c4df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 23 Apr 2024 17:27:49 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates
# Fri, 26 Apr 2024 22:08:23 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 22:08:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf
# Fri, 26 Apr 2024 22:08:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 26 Apr 2024 22:08:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 26 Apr 2024 22:08:29 GMT
EXPOSE 8888
# Fri, 26 Apr 2024 22:08:29 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 22:08:29 GMT
COPY file:1f6f0a0b9c49483e5400adfe0e7eddaca76d6a690f01cf0288b90406e2da965c in /entrypoint.sh 
# Fri, 26 Apr 2024 22:08:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 22:08:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec84f8c4b4c91fcb32de58f4c3ad4f074277a222c69804bc60e3dc52fb9edb0`  
		Last Modified: Sat, 16 Mar 2024 03:21:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9451ab070e66261dde2ccade99194ed606e0d2cfd54f79ada2502c394614520c`  
		Last Modified: Tue, 23 Apr 2024 17:28:34 GMT  
		Size: 295.9 KB (295868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546a8b82c5fb489b1dbf78396994620fdcecfaa11ecaf898cb28c9be6454ba02`  
		Last Modified: Fri, 26 Apr 2024 22:09:15 GMT  
		Size: 27.9 MB (27866936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e91faf745cc56c62ba29f9b761f676feff9fcb6ef2bdd744aa8aa6ea6d9e41`  
		Last Modified: Fri, 26 Apr 2024 22:09:11 GMT  
		Size: 12.3 KB (12266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747ae52b83e8dcb5ec955776e51f45ab29101447a4355ac52c7d95df3bdc4306`  
		Last Modified: Fri, 26 Apr 2024 22:09:10 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0963e152ee8236f28dfafb48dc75f73db4336c8c1303e13071ba6f0052367f4a`  
		Last Modified: Fri, 26 Apr 2024 22:09:11 GMT  
		Size: 292.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.4`

```console
$ docker pull chronograf@sha256:00212cde3ec0e7e03064c97967b652a3ccad715a75272d56b16eeb70414f6152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10.4` - linux; amd64

```console
$ docker pull chronograf@sha256:392c73fd8092f3be72138161975602b6f411a9231b383ce307a8c53e1b292b87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84462839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df456f2e4a0292d497a44d2682d4e00eeeedaafa6b3464dfb2d8b906f2c87d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:54:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 26 Apr 2024 22:08:10 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 22:08:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 26 Apr 2024 22:08:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 26 Apr 2024 22:08:18 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 26 Apr 2024 22:08:18 GMT
EXPOSE 8888
# Fri, 26 Apr 2024 22:08:18 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 22:08:18 GMT
COPY file:322ec550f2fba037831462da9d81d40f7e6c1c94797662b6e166f5d8d36c5b4e in /entrypoint.sh 
# Fri, 26 Apr 2024 22:08:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 22:08:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f2b6422b4a4d96ef0937dc3f999ca0e9a3d3c511bb569f06dabd00917fb88c`  
		Last Modified: Wed, 24 Apr 2024 07:55:22 GMT  
		Size: 7.9 MB (7873309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd8036513aebcbc1aa0503e1eea934239be55bfba53a905f7e2f330f3eb098b`  
		Last Modified: Fri, 26 Apr 2024 22:09:00 GMT  
		Size: 47.4 MB (47414583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898f59b0daa71b77057c779cd4332f4f21f234f0a7f4d7fb396f0c80607788fa`  
		Last Modified: Fri, 26 Apr 2024 22:08:54 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8dc3abe6e300121116e074d1f11f2ac81cbca3b64b2ada8d39bad1ad88fa3a`  
		Last Modified: Fri, 26 Apr 2024 22:08:54 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a177aec86da3c2e057f5f2b64f712e5d1eb9ce89895689ea7009e03de8d2e97`  
		Last Modified: Fri, 26 Apr 2024 22:08:54 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ff93bd9576060dc03a733fd949b2138b6f22a702812151c683edb1b074c63534
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75744378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e27f95eef0625e76a75f07f71d1e2ec121ada9b126ecd4cb001f8d7fa58164`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:48:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 26 Apr 2024 21:59:12 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 21:59:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 26 Apr 2024 21:59:28 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 26 Apr 2024 21:59:28 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 26 Apr 2024 21:59:28 GMT
EXPOSE 8888
# Fri, 26 Apr 2024 21:59:29 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 21:59:29 GMT
COPY file:322ec550f2fba037831462da9d81d40f7e6c1c94797662b6e166f5d8d36c5b4e in /entrypoint.sh 
# Fri, 26 Apr 2024 21:59:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 21:59:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c215aa1ee7dcb414d32d3379d194e0898aeb361148172b49be795e68955e0e6c`  
		Last Modified: Wed, 24 Apr 2024 04:49:20 GMT  
		Size: 6.5 MB (6497997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6652e0b271a4a516ee18f95969d55d8ff1c5e99fab60cd88381e0f92d47df64`  
		Last Modified: Fri, 26 Apr 2024 21:59:55 GMT  
		Size: 44.5 MB (44481468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd921d46385df6c1e4aeb94f04b6a87469a8734325cf5f4f23f14fc5b4fc4d00`  
		Last Modified: Fri, 26 Apr 2024 21:59:46 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8b8a0ecd7b222ce7c45a000b9fae64800ce777eb742cf4ad017ed41c9a6e98`  
		Last Modified: Fri, 26 Apr 2024 21:59:46 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdea724c673507feacd1f1647b5710a94c0962eb15d34b499fb922e402a0f64e`  
		Last Modified: Fri, 26 Apr 2024 21:59:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ef62f8997e8e2908f40073336f7f3ecae0f2d4b873e5eaccf4a0bf1fd0932bfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82039807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e687daa3d3a56538e9daff12e27a705bfbee3f9f1e53f9a0cf30a89b3fb74fcf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 11:12:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 29 Apr 2024 19:59:09 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Mon, 29 Apr 2024 19:59:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 29 Apr 2024 19:59:17 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 29 Apr 2024 19:59:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 29 Apr 2024 19:59:17 GMT
EXPOSE 8888
# Mon, 29 Apr 2024 19:59:17 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Apr 2024 19:59:17 GMT
COPY file:322ec550f2fba037831462da9d81d40f7e6c1c94797662b6e166f5d8d36c5b4e in /entrypoint.sh 
# Mon, 29 Apr 2024 19:59:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Apr 2024 19:59:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3777eaa448d12fa64be79faf0defd5c860f34e6f5785fc5e34b07bd082d784e1`  
		Last Modified: Wed, 24 Apr 2024 11:13:49 GMT  
		Size: 7.6 MB (7649956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9ecf2bddea629649f67d6e6b64ef35f9be939d68ec2fbd9ab4551ac08d0b70`  
		Last Modified: Mon, 29 Apr 2024 19:59:37 GMT  
		Size: 45.2 MB (45185447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b736e8a28ad4ff6c1484f1c6c86899d318f86c8ce53512c3b1e7e9cc7c6cca`  
		Last Modified: Mon, 29 Apr 2024 19:59:31 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66938160c27eb30ea21022ebae3accbc0611e3ec21216bfbb79b93995efb0651`  
		Last Modified: Mon, 29 Apr 2024 19:59:32 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e699ac1e7152c5f174ebd82e9650342f1e2d7a79f4ebfa183934588058b6ebb`  
		Last Modified: Mon, 29 Apr 2024 19:59:31 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.4-alpine`

```console
$ docker pull chronograf@sha256:bc677d048b78b7ee3b2339fea88440e7e1e6f36c322adbceaef16bbd4cdd7c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:e4d3d65dfa3b17d25170a680c6e9bb88c2ffc649a7eea1af1b9512d127f61561
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31590092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1aa448b8cb627fb1b3de3e95e85d1792fb7c84a2324e6bacc6cf6f2bd1c4df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 23 Apr 2024 17:27:49 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates
# Fri, 26 Apr 2024 22:08:23 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 22:08:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf
# Fri, 26 Apr 2024 22:08:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 26 Apr 2024 22:08:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 26 Apr 2024 22:08:29 GMT
EXPOSE 8888
# Fri, 26 Apr 2024 22:08:29 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 22:08:29 GMT
COPY file:1f6f0a0b9c49483e5400adfe0e7eddaca76d6a690f01cf0288b90406e2da965c in /entrypoint.sh 
# Fri, 26 Apr 2024 22:08:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 22:08:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec84f8c4b4c91fcb32de58f4c3ad4f074277a222c69804bc60e3dc52fb9edb0`  
		Last Modified: Sat, 16 Mar 2024 03:21:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9451ab070e66261dde2ccade99194ed606e0d2cfd54f79ada2502c394614520c`  
		Last Modified: Tue, 23 Apr 2024 17:28:34 GMT  
		Size: 295.9 KB (295868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546a8b82c5fb489b1dbf78396994620fdcecfaa11ecaf898cb28c9be6454ba02`  
		Last Modified: Fri, 26 Apr 2024 22:09:15 GMT  
		Size: 27.9 MB (27866936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e91faf745cc56c62ba29f9b761f676feff9fcb6ef2bdd744aa8aa6ea6d9e41`  
		Last Modified: Fri, 26 Apr 2024 22:09:11 GMT  
		Size: 12.3 KB (12266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747ae52b83e8dcb5ec955776e51f45ab29101447a4355ac52c7d95df3bdc4306`  
		Last Modified: Fri, 26 Apr 2024 22:09:10 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0963e152ee8236f28dfafb48dc75f73db4336c8c1303e13071ba6f0052367f4a`  
		Last Modified: Fri, 26 Apr 2024 22:09:11 GMT  
		Size: 292.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:ce2a34647d8e76d242b82d0226f6cd001212808c4bc5363f4f1f464efcb31925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:5bbd3f1a0a7efaa8b58285b9b66adf1a76f3ee5fa2597d05256f93ad12e03514
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70615580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614e7cc95f0df6d45c26c77c745abbc7c962fba31514a8e6272ef126fd144046`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:52:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 07:53:00 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 24 Apr 2024 07:53:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 07:53:08 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Apr 2024 07:53:08 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Apr 2024 07:53:08 GMT
EXPOSE 8888
# Wed, 24 Apr 2024 07:53:09 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Apr 2024 07:53:09 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 24 Apr 2024 07:53:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 07:53:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9339058768ee21ef14db4a6e5539396464d6849fe81d5d137cc0f31ed28d6ae7`  
		Last Modified: Wed, 24 Apr 2024 07:54:38 GMT  
		Size: 4.4 MB (4417257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18518d357101f0336be7aed001dc6dfb6dc2d0ef5165a686aa479bc3d6390fe`  
		Last Modified: Wed, 24 Apr 2024 07:54:45 GMT  
		Size: 34.7 MB (34739656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372762a5c67c34ebd0733dec6b7022246b565688fa8dbd261b8e22d4d597de1c`  
		Last Modified: Wed, 24 Apr 2024 07:54:37 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e4c48d97612a7925ae3e0dc825354e151e5463f260117397377aed3d720fe9`  
		Last Modified: Wed, 24 Apr 2024 07:54:37 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4d48ec075aeab31682e475ab19bac5038cf6cd5972f4d58863fc5e7647a66c`  
		Last Modified: Wed, 24 Apr 2024 07:54:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:debd57dad7661433e9f7f67f238607b547397b2ecd8ac905e36278f3f5d57204
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63438370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321f4a8f51fca1529183809226495b960877c8c49fa1b82cef12f6cdb4f80046`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:25 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Wed, 24 Apr 2024 04:07:25 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:47:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 04:47:15 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 24 Apr 2024 04:47:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 04:47:26 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Apr 2024 04:47:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Apr 2024 04:47:27 GMT
EXPOSE 8888
# Wed, 24 Apr 2024 04:47:27 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Apr 2024 04:47:27 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 24 Apr 2024 04:47:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 04:47:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ce5e2bda7f1b733adce79f3ea848923f62b2c01e9fdff2f5e5a1a4135f8111`  
		Last Modified: Wed, 24 Apr 2024 04:48:40 GMT  
		Size: 3.7 MB (3719748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8b25aacfe761549c1d9608d6a98985880edf8a1bd10e8f85ed948d54d77064`  
		Last Modified: Wed, 24 Apr 2024 04:48:44 GMT  
		Size: 33.1 MB (33099478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ec803085c6af82927fa717020c3f124775016303659ddaf02475123ec726fd`  
		Last Modified: Wed, 24 Apr 2024 04:48:40 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf01307f2af88317af41c4a0a965028db5ffe3f8f07720a935bc61b2b4c5d80`  
		Last Modified: Wed, 24 Apr 2024 04:48:40 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315a0dee2d7b8b22a3444771859fbe65d9cad606c869fb1946b29762cd41e9e`  
		Last Modified: Wed, 24 Apr 2024 04:48:40 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:81fb01f13dae9f7935087d29d190c0f6fa298b8fb7b259e8d90e3d5e8d30f68b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67770491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d349c167de81af6e56ded01c77cddfca48d7d017cb458d3df12425b0e321d5d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 11:12:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 11:12:04 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 24 Apr 2024 11:12:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 11:12:12 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Apr 2024 11:12:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Apr 2024 11:12:12 GMT
EXPOSE 8888
# Wed, 24 Apr 2024 11:12:12 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Apr 2024 11:12:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 24 Apr 2024 11:12:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 11:12:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9768d7e50e3c3561567843fbad356f79da75cb39d997e4872860f632f2fd3751`  
		Last Modified: Wed, 24 Apr 2024 11:13:15 GMT  
		Size: 4.4 MB (4418893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56754a0fecdd798da27d7564133674f66d024d9203441c6b39bc9d0bcbab6084`  
		Last Modified: Wed, 24 Apr 2024 11:13:17 GMT  
		Size: 33.2 MB (33239855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dc188b9eefc557855528e062c30b6490ebc2ef18bede1bb754c04e8e24482b`  
		Last Modified: Wed, 24 Apr 2024 11:13:14 GMT  
		Size: 12.3 KB (12254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7fe91376e8a958bb5a8e9d1f75367fb453375ad7b0f4188e142195fb3c3b7e`  
		Last Modified: Wed, 24 Apr 2024 11:13:14 GMT  
		Size: 11.9 KB (11913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7aaf04637358d616b1a09b1727b8b78070f11b2542d10c291804da2021496b`  
		Last Modified: Wed, 24 Apr 2024 11:13:14 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:7cc77100ae752f9c44461fe06b8aeee4d2bc196a7600f33aecfbe22d60da8df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ff6e911fb57a1c911356978496ae4e19ce5a0071aa819daed26437c635ab9dbc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23246247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591c051e96ac4e4633bc4f6731af433d301e815e3568351cf4e532609a3921a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:20:06 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 03:20:06 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 16 Mar 2024 03:20:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 03:20:11 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 16 Mar 2024 03:20:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 16 Mar 2024 03:20:12 GMT
EXPOSE 8888
# Sat, 16 Mar 2024 03:20:12 GMT
VOLUME [/var/lib/chronograf]
# Sat, 16 Mar 2024 03:20:12 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 16 Mar 2024 03:20:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 03:20:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98004ffc28465fb13a09790c0b8d8af0ed002fa6fa8a93c0bfc098bb1862afb1`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 284.9 KB (284942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938fcaa198dc21c9b821d611166b80842631f50fe715a8f272172cafe3176814`  
		Last Modified: Sat, 16 Mar 2024 03:21:14 GMT  
		Size: 19.6 MB (19557218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266bc6e6efce66b509e7e8eca65e5ce23597892fb4f4560ce39cc6b2aad485d`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecf86d2f3fd6fc7c346b9659e0544173a1f9ab6b9aea84772c67cbb86bb4a3b`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e40de9b3fe95133a27a754000d8ba962b35b7bbf336e140ed9094c463b2073`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:ce2a34647d8e76d242b82d0226f6cd001212808c4bc5363f4f1f464efcb31925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:5bbd3f1a0a7efaa8b58285b9b66adf1a76f3ee5fa2597d05256f93ad12e03514
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70615580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614e7cc95f0df6d45c26c77c745abbc7c962fba31514a8e6272ef126fd144046`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:52:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 07:53:00 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 24 Apr 2024 07:53:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 07:53:08 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Apr 2024 07:53:08 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Apr 2024 07:53:08 GMT
EXPOSE 8888
# Wed, 24 Apr 2024 07:53:09 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Apr 2024 07:53:09 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 24 Apr 2024 07:53:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 07:53:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9339058768ee21ef14db4a6e5539396464d6849fe81d5d137cc0f31ed28d6ae7`  
		Last Modified: Wed, 24 Apr 2024 07:54:38 GMT  
		Size: 4.4 MB (4417257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18518d357101f0336be7aed001dc6dfb6dc2d0ef5165a686aa479bc3d6390fe`  
		Last Modified: Wed, 24 Apr 2024 07:54:45 GMT  
		Size: 34.7 MB (34739656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372762a5c67c34ebd0733dec6b7022246b565688fa8dbd261b8e22d4d597de1c`  
		Last Modified: Wed, 24 Apr 2024 07:54:37 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e4c48d97612a7925ae3e0dc825354e151e5463f260117397377aed3d720fe9`  
		Last Modified: Wed, 24 Apr 2024 07:54:37 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4d48ec075aeab31682e475ab19bac5038cf6cd5972f4d58863fc5e7647a66c`  
		Last Modified: Wed, 24 Apr 2024 07:54:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:debd57dad7661433e9f7f67f238607b547397b2ecd8ac905e36278f3f5d57204
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63438370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321f4a8f51fca1529183809226495b960877c8c49fa1b82cef12f6cdb4f80046`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:25 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Wed, 24 Apr 2024 04:07:25 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:47:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 04:47:15 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 24 Apr 2024 04:47:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 04:47:26 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Apr 2024 04:47:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Apr 2024 04:47:27 GMT
EXPOSE 8888
# Wed, 24 Apr 2024 04:47:27 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Apr 2024 04:47:27 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 24 Apr 2024 04:47:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 04:47:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ce5e2bda7f1b733adce79f3ea848923f62b2c01e9fdff2f5e5a1a4135f8111`  
		Last Modified: Wed, 24 Apr 2024 04:48:40 GMT  
		Size: 3.7 MB (3719748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8b25aacfe761549c1d9608d6a98985880edf8a1bd10e8f85ed948d54d77064`  
		Last Modified: Wed, 24 Apr 2024 04:48:44 GMT  
		Size: 33.1 MB (33099478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ec803085c6af82927fa717020c3f124775016303659ddaf02475123ec726fd`  
		Last Modified: Wed, 24 Apr 2024 04:48:40 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf01307f2af88317af41c4a0a965028db5ffe3f8f07720a935bc61b2b4c5d80`  
		Last Modified: Wed, 24 Apr 2024 04:48:40 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315a0dee2d7b8b22a3444771859fbe65d9cad606c869fb1946b29762cd41e9e`  
		Last Modified: Wed, 24 Apr 2024 04:48:40 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:81fb01f13dae9f7935087d29d190c0f6fa298b8fb7b259e8d90e3d5e8d30f68b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67770491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d349c167de81af6e56ded01c77cddfca48d7d017cb458d3df12425b0e321d5d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 11:12:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 11:12:04 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 24 Apr 2024 11:12:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 11:12:12 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Apr 2024 11:12:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Apr 2024 11:12:12 GMT
EXPOSE 8888
# Wed, 24 Apr 2024 11:12:12 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Apr 2024 11:12:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 24 Apr 2024 11:12:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 11:12:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9768d7e50e3c3561567843fbad356f79da75cb39d997e4872860f632f2fd3751`  
		Last Modified: Wed, 24 Apr 2024 11:13:15 GMT  
		Size: 4.4 MB (4418893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56754a0fecdd798da27d7564133674f66d024d9203441c6b39bc9d0bcbab6084`  
		Last Modified: Wed, 24 Apr 2024 11:13:17 GMT  
		Size: 33.2 MB (33239855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dc188b9eefc557855528e062c30b6490ebc2ef18bede1bb754c04e8e24482b`  
		Last Modified: Wed, 24 Apr 2024 11:13:14 GMT  
		Size: 12.3 KB (12254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7fe91376e8a958bb5a8e9d1f75367fb453375ad7b0f4188e142195fb3c3b7e`  
		Last Modified: Wed, 24 Apr 2024 11:13:14 GMT  
		Size: 11.9 KB (11913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7aaf04637358d616b1a09b1727b8b78070f11b2542d10c291804da2021496b`  
		Last Modified: Wed, 24 Apr 2024 11:13:14 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:7cc77100ae752f9c44461fe06b8aeee4d2bc196a7600f33aecfbe22d60da8df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ff6e911fb57a1c911356978496ae4e19ce5a0071aa819daed26437c635ab9dbc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23246247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591c051e96ac4e4633bc4f6731af433d301e815e3568351cf4e532609a3921a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:20:06 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 03:20:06 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 16 Mar 2024 03:20:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 03:20:11 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 16 Mar 2024 03:20:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 16 Mar 2024 03:20:12 GMT
EXPOSE 8888
# Sat, 16 Mar 2024 03:20:12 GMT
VOLUME [/var/lib/chronograf]
# Sat, 16 Mar 2024 03:20:12 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 16 Mar 2024 03:20:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 03:20:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98004ffc28465fb13a09790c0b8d8af0ed002fa6fa8a93c0bfc098bb1862afb1`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 284.9 KB (284942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938fcaa198dc21c9b821d611166b80842631f50fe715a8f272172cafe3176814`  
		Last Modified: Sat, 16 Mar 2024 03:21:14 GMT  
		Size: 19.6 MB (19557218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266bc6e6efce66b509e7e8eca65e5ce23597892fb4f4560ce39cc6b2aad485d`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecf86d2f3fd6fc7c346b9659e0544173a1f9ab6b9aea84772c67cbb86bb4a3b`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e40de9b3fe95133a27a754000d8ba962b35b7bbf336e140ed9094c463b2073`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:4b5266fbf35533bc308ba585d7b68434b3b85d530d58a0c84e209c810e04626e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:6d0485f621b853a4891779f16aeaaef0a39ce8b1d9aa79c8ef5e0fbe9c83725e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71267756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d760e8a0ba057d62de6e00eb68bc74103fddc837fd6854c45f653e0e3dbbc24`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:53:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 07:53:24 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 24 Apr 2024 07:53:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 07:53:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Apr 2024 07:53:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Apr 2024 07:53:34 GMT
EXPOSE 8888
# Wed, 24 Apr 2024 07:53:34 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Apr 2024 07:53:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 24 Apr 2024 07:53:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 07:53:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520be706950d35ea5e8a6d3289b038934be63cb5ed7dc0adfe502c822c248c6d`  
		Last Modified: Wed, 24 Apr 2024 07:54:54 GMT  
		Size: 5.2 MB (5228344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce337564de98a06fe40df070cb65cfa4d32fc62c44fdb8f8a6da352ff85171d0`  
		Last Modified: Wed, 24 Apr 2024 07:54:58 GMT  
		Size: 34.6 MB (34580751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45799c97732622190d6b1c46c1efa3c1f0aa2bf11a76e1ba3a2886d2fe715508`  
		Last Modified: Wed, 24 Apr 2024 07:54:53 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9708d430bcb4cd1be2010a683fa8f764d6c05f66a87b29e8b10dbf8510600996`  
		Last Modified: Wed, 24 Apr 2024 07:54:53 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d205b12e20a9c4f608afa696e40f601f59fef304febe7fc70f5982a6aeec842`  
		Last Modified: Wed, 24 Apr 2024 07:54:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:88ab78b25d44bdcbd7359d8102e3ec7e93b453da3a077557ad43d25f070e2ee1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63864672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5495d9a69fdb6ae84bfe97c3787f187a84c823953280282af5ee94514086e7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:25 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Wed, 24 Apr 2024 04:07:25 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:47:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 04:47:37 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 24 Apr 2024 04:47:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 04:47:46 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Apr 2024 04:47:46 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Apr 2024 04:47:46 GMT
EXPOSE 8888
# Wed, 24 Apr 2024 04:47:46 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Apr 2024 04:47:46 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 24 Apr 2024 04:47:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 04:47:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b871ba8c2778591f604a672382ac37360b43952a34eb6a05b91baa8a39132a0`  
		Last Modified: Wed, 24 Apr 2024 04:48:53 GMT  
		Size: 4.5 MB (4493435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef280536e4bda48fd5aa60d5f29e957ddb2b4e4954b994d81d850774bc72bf02`  
		Last Modified: Wed, 24 Apr 2024 04:48:57 GMT  
		Size: 32.8 MB (32752097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4929bdd506f5b5eb3983087ece8a56bb8cc09b8f95bf92718e7abb358b4c8408`  
		Last Modified: Wed, 24 Apr 2024 04:48:52 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b42dbcbd77de125f23f644d24c1faecf49122be71125c523d70e33233e7e8d1`  
		Last Modified: Wed, 24 Apr 2024 04:48:52 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22692e20f6351a0695cea2302b569c3e77558eb3314fa1f286b904e029aa94f5`  
		Last Modified: Wed, 24 Apr 2024 04:48:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5f75bf0c7d06ba95406e56a0f9c87dd38f7a7c164b591baff100e6cb1983e197
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67968456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f652c95bb6cb3b396b96a203a3075a04c02bf6a1928af1cd9b859eb4abbc6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 11:12:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 11:12:22 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 24 Apr 2024 11:12:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 11:12:32 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Apr 2024 11:12:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Apr 2024 11:12:32 GMT
EXPOSE 8888
# Wed, 24 Apr 2024 11:12:32 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Apr 2024 11:12:32 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 24 Apr 2024 11:12:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 11:12:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9970cd3c9ba98c288db4431779cc3c04c36809c5b9099409912a1d0954eafe7`  
		Last Modified: Wed, 24 Apr 2024 11:13:26 GMT  
		Size: 5.2 MB (5210732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f4dfec480a5b366f495df1f027bf7502c8f5e89e4df602dee6882e5a16e6b0`  
		Last Modified: Wed, 24 Apr 2024 11:13:28 GMT  
		Size: 32.6 MB (32645987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e6a6094df615764cf70ef1464b3d7f83705160fcee8770c35a3a8b82e6ea4f`  
		Last Modified: Wed, 24 Apr 2024 11:13:25 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c055861580dc2ec1fe55509dc5acd032ad1d229ae3a4cbe4d5f469d3913030`  
		Last Modified: Wed, 24 Apr 2024 11:13:25 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3e6b0cc1bec78a4108123bb4017f14265983b4deb8218f4b12b964a3a80c0a`  
		Last Modified: Wed, 24 Apr 2024 11:13:26 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:f86b9c1882c523515c80d656b0ebdbf97d0591f86d4ad35b6c2d41af9d4d6e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4e405e1032ae084ea4091b135168c25b345399d30879e6aafbc3861de36d803e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22893187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76ad514ca513592ec7ac47b5fb9dc6c033299f933ff5b456706545a69b4b1d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:20:06 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 03:20:19 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sat, 16 Mar 2024 03:20:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 03:20:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 16 Mar 2024 03:20:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 16 Mar 2024 03:20:25 GMT
EXPOSE 8888
# Sat, 16 Mar 2024 03:20:25 GMT
VOLUME [/var/lib/chronograf]
# Sat, 16 Mar 2024 03:20:25 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 16 Mar 2024 03:20:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 03:20:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98004ffc28465fb13a09790c0b8d8af0ed002fa6fa8a93c0bfc098bb1862afb1`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 284.9 KB (284942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4cc01a94fafcaa370de6eb1d82920490e8b7bad16c2eaa40918e3a9fad57e1`  
		Last Modified: Sat, 16 Mar 2024 03:21:26 GMT  
		Size: 19.2 MB (19204158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2e39810281cb32653a738bf6e8e1949692a93c19dcc6ea1af683671af9f58c`  
		Last Modified: Sat, 16 Mar 2024 03:21:23 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5290c71eb9dd78e6d62ced897c4ec0ba8880d660722b1e56a6b8769ca100841`  
		Last Modified: Sat, 16 Mar 2024 03:21:23 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac68863d78379d68261e2d0188f4da0241ac15bf7d368e2a034e5639eadc08`  
		Last Modified: Sat, 16 Mar 2024 03:21:23 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:4b5266fbf35533bc308ba585d7b68434b3b85d530d58a0c84e209c810e04626e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:6d0485f621b853a4891779f16aeaaef0a39ce8b1d9aa79c8ef5e0fbe9c83725e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71267756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d760e8a0ba057d62de6e00eb68bc74103fddc837fd6854c45f653e0e3dbbc24`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:53:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 07:53:24 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 24 Apr 2024 07:53:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 07:53:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Apr 2024 07:53:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Apr 2024 07:53:34 GMT
EXPOSE 8888
# Wed, 24 Apr 2024 07:53:34 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Apr 2024 07:53:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 24 Apr 2024 07:53:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 07:53:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520be706950d35ea5e8a6d3289b038934be63cb5ed7dc0adfe502c822c248c6d`  
		Last Modified: Wed, 24 Apr 2024 07:54:54 GMT  
		Size: 5.2 MB (5228344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce337564de98a06fe40df070cb65cfa4d32fc62c44fdb8f8a6da352ff85171d0`  
		Last Modified: Wed, 24 Apr 2024 07:54:58 GMT  
		Size: 34.6 MB (34580751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45799c97732622190d6b1c46c1efa3c1f0aa2bf11a76e1ba3a2886d2fe715508`  
		Last Modified: Wed, 24 Apr 2024 07:54:53 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9708d430bcb4cd1be2010a683fa8f764d6c05f66a87b29e8b10dbf8510600996`  
		Last Modified: Wed, 24 Apr 2024 07:54:53 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d205b12e20a9c4f608afa696e40f601f59fef304febe7fc70f5982a6aeec842`  
		Last Modified: Wed, 24 Apr 2024 07:54:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:88ab78b25d44bdcbd7359d8102e3ec7e93b453da3a077557ad43d25f070e2ee1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63864672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5495d9a69fdb6ae84bfe97c3787f187a84c823953280282af5ee94514086e7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:25 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Wed, 24 Apr 2024 04:07:25 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:47:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 04:47:37 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 24 Apr 2024 04:47:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 04:47:46 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Apr 2024 04:47:46 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Apr 2024 04:47:46 GMT
EXPOSE 8888
# Wed, 24 Apr 2024 04:47:46 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Apr 2024 04:47:46 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 24 Apr 2024 04:47:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 04:47:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b871ba8c2778591f604a672382ac37360b43952a34eb6a05b91baa8a39132a0`  
		Last Modified: Wed, 24 Apr 2024 04:48:53 GMT  
		Size: 4.5 MB (4493435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef280536e4bda48fd5aa60d5f29e957ddb2b4e4954b994d81d850774bc72bf02`  
		Last Modified: Wed, 24 Apr 2024 04:48:57 GMT  
		Size: 32.8 MB (32752097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4929bdd506f5b5eb3983087ece8a56bb8cc09b8f95bf92718e7abb358b4c8408`  
		Last Modified: Wed, 24 Apr 2024 04:48:52 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b42dbcbd77de125f23f644d24c1faecf49122be71125c523d70e33233e7e8d1`  
		Last Modified: Wed, 24 Apr 2024 04:48:52 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22692e20f6351a0695cea2302b569c3e77558eb3314fa1f286b904e029aa94f5`  
		Last Modified: Wed, 24 Apr 2024 04:48:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5f75bf0c7d06ba95406e56a0f9c87dd38f7a7c164b591baff100e6cb1983e197
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67968456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f652c95bb6cb3b396b96a203a3075a04c02bf6a1928af1cd9b859eb4abbc6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 11:12:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 11:12:22 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 24 Apr 2024 11:12:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 11:12:32 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Apr 2024 11:12:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Apr 2024 11:12:32 GMT
EXPOSE 8888
# Wed, 24 Apr 2024 11:12:32 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Apr 2024 11:12:32 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 24 Apr 2024 11:12:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 11:12:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9970cd3c9ba98c288db4431779cc3c04c36809c5b9099409912a1d0954eafe7`  
		Last Modified: Wed, 24 Apr 2024 11:13:26 GMT  
		Size: 5.2 MB (5210732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f4dfec480a5b366f495df1f027bf7502c8f5e89e4df602dee6882e5a16e6b0`  
		Last Modified: Wed, 24 Apr 2024 11:13:28 GMT  
		Size: 32.6 MB (32645987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e6a6094df615764cf70ef1464b3d7f83705160fcee8770c35a3a8b82e6ea4f`  
		Last Modified: Wed, 24 Apr 2024 11:13:25 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c055861580dc2ec1fe55509dc5acd032ad1d229ae3a4cbe4d5f469d3913030`  
		Last Modified: Wed, 24 Apr 2024 11:13:25 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3e6b0cc1bec78a4108123bb4017f14265983b4deb8218f4b12b964a3a80c0a`  
		Last Modified: Wed, 24 Apr 2024 11:13:26 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:f86b9c1882c523515c80d656b0ebdbf97d0591f86d4ad35b6c2d41af9d4d6e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4e405e1032ae084ea4091b135168c25b345399d30879e6aafbc3861de36d803e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22893187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76ad514ca513592ec7ac47b5fb9dc6c033299f933ff5b456706545a69b4b1d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:20:06 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 03:20:19 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sat, 16 Mar 2024 03:20:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 03:20:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 16 Mar 2024 03:20:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 16 Mar 2024 03:20:25 GMT
EXPOSE 8888
# Sat, 16 Mar 2024 03:20:25 GMT
VOLUME [/var/lib/chronograf]
# Sat, 16 Mar 2024 03:20:25 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 16 Mar 2024 03:20:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 03:20:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98004ffc28465fb13a09790c0b8d8af0ed002fa6fa8a93c0bfc098bb1862afb1`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 284.9 KB (284942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4cc01a94fafcaa370de6eb1d82920490e8b7bad16c2eaa40918e3a9fad57e1`  
		Last Modified: Sat, 16 Mar 2024 03:21:26 GMT  
		Size: 19.2 MB (19204158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2e39810281cb32653a738bf6e8e1949692a93c19dcc6ea1af683671af9f58c`  
		Last Modified: Sat, 16 Mar 2024 03:21:23 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5290c71eb9dd78e6d62ced897c4ec0ba8880d660722b1e56a6b8769ca100841`  
		Last Modified: Sat, 16 Mar 2024 03:21:23 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac68863d78379d68261e2d0188f4da0241ac15bf7d368e2a034e5639eadc08`  
		Last Modified: Sat, 16 Mar 2024 03:21:23 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:cff878efc147e8d2e5d44d35e648df3d94ec338fc6421add7d218d28e2f36337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:96f6c77c07709a3d5bd835e235273cc673c931519be22ce7fc7e1ac9cb9d319b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71915276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90be9674d59f7c548632114deb86d96b1814a7e3b1efe7afdab747410558d61b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:53:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 07:53:40 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 24 Apr 2024 07:53:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 07:53:51 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Apr 2024 07:53:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Apr 2024 07:53:51 GMT
EXPOSE 8888
# Wed, 24 Apr 2024 07:53:51 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Apr 2024 07:53:51 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 24 Apr 2024 07:53:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 07:53:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520be706950d35ea5e8a6d3289b038934be63cb5ed7dc0adfe502c822c248c6d`  
		Last Modified: Wed, 24 Apr 2024 07:54:54 GMT  
		Size: 5.2 MB (5228344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d206190a9d9ab39d3fe0b30d60c2423e6c2972c800400818684f2193b2c92f5`  
		Last Modified: Wed, 24 Apr 2024 07:55:11 GMT  
		Size: 35.2 MB (35228266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac6c0296c98c70367e5edeb0c04b3e149ccb881367aa1050a4923cfca635ef1`  
		Last Modified: Wed, 24 Apr 2024 07:55:07 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb3cf3503e58f50444e8696d20eb1223f3fe3539685ca2de1fb5813adcaafff`  
		Last Modified: Wed, 24 Apr 2024 07:55:07 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7669f20d3f017b13c835da2e7736f4113669a288a0e3773b1435c876e44f274a`  
		Last Modified: Wed, 24 Apr 2024 07:55:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b99b18c80d1f1a91ffcda6d01fc1e102da0ede7771e4dc7afeee3591fd40ab00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64640752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8e448c13ead4c39b4233d16bf661f76baa83412eb466e13382fad9ff61a045`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:25 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Wed, 24 Apr 2024 04:07:25 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:47:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 04:47:49 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 24 Apr 2024 04:48:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 04:48:01 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Apr 2024 04:48:01 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Apr 2024 04:48:01 GMT
EXPOSE 8888
# Wed, 24 Apr 2024 04:48:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Apr 2024 04:48:02 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 24 Apr 2024 04:48:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 04:48:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b871ba8c2778591f604a672382ac37360b43952a34eb6a05b91baa8a39132a0`  
		Last Modified: Wed, 24 Apr 2024 04:48:53 GMT  
		Size: 4.5 MB (4493435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048e129e94db61beff840eec865569072a5d891bafa56496f675615cb9f06b4a`  
		Last Modified: Wed, 24 Apr 2024 04:49:10 GMT  
		Size: 33.5 MB (33528177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1611f02b2c0f442207d7ee4a156bf66fa255552a3e19c7cbf645ed0c83e078`  
		Last Modified: Wed, 24 Apr 2024 04:49:05 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8aa019799e948c99796e0c8f91bbbf68feeae61068fa36a7233d3025c8bc26`  
		Last Modified: Wed, 24 Apr 2024 04:49:05 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb1672e07cf7fc6a172f4faf7c4b2b29b85becaf9d075ca0caf09f8fd052b1c`  
		Last Modified: Wed, 24 Apr 2024 04:49:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:93a21fd0cf886d03724f40fa7f206a36c3b8ce33db7a012c964c855ff048a244
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68720754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4766feb604fd85b210f245bc7968225376ea93b7ec107a1bb885e3055a66e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 11:12:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 11:12:35 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 24 Apr 2024 11:12:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 11:12:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Apr 2024 11:12:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Apr 2024 11:12:42 GMT
EXPOSE 8888
# Wed, 24 Apr 2024 11:12:42 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Apr 2024 11:12:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 24 Apr 2024 11:12:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 11:12:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9970cd3c9ba98c288db4431779cc3c04c36809c5b9099409912a1d0954eafe7`  
		Last Modified: Wed, 24 Apr 2024 11:13:26 GMT  
		Size: 5.2 MB (5210732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e4a1cd79dcbead26f1a4fa4b98707ec8db81712ea765cd1e18dcab1771729f`  
		Last Modified: Wed, 24 Apr 2024 11:13:40 GMT  
		Size: 33.4 MB (33398285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4cd6d69300a0bb070b26147a6db193a3a7913e5958651df0f6ff711960ea79`  
		Last Modified: Wed, 24 Apr 2024 11:13:37 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae1411567fc1c9c3ef4541ab396383fe8d5ad09048636836c33e1b729f35f4`  
		Last Modified: Wed, 24 Apr 2024 11:13:37 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477b95c5e8625010c1cc1ca7c9030edb403c68c9731c23e7c44b4b68a48352d0`  
		Last Modified: Wed, 24 Apr 2024 11:13:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:58038f3e5f95b38efbe31e2dd8c7b7c0da7a926da9b6ee6845699869095111a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c25d48417f45446f783c5adf64c42c1d76444df716f79ea61f71db2172028923
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23361283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cd392d9f55a4830d355e0f9b6d013cadc65691db4951a14030c9261717c704`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:20:06 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 03:20:32 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sat, 16 Mar 2024 03:20:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 03:20:38 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 16 Mar 2024 03:20:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 16 Mar 2024 03:20:38 GMT
EXPOSE 8888
# Sat, 16 Mar 2024 03:20:38 GMT
VOLUME [/var/lib/chronograf]
# Sat, 16 Mar 2024 03:20:38 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 16 Mar 2024 03:20:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 03:20:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98004ffc28465fb13a09790c0b8d8af0ed002fa6fa8a93c0bfc098bb1862afb1`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 284.9 KB (284942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ad7820274585078b0e98dff9ca0a6a138b48fa805200be362ae835e55d935e`  
		Last Modified: Sat, 16 Mar 2024 03:21:38 GMT  
		Size: 19.7 MB (19672268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10615eac7f71b29e6e8a49969cc83939de885312ca46c1b7c853a6986226fc1d`  
		Last Modified: Sat, 16 Mar 2024 03:21:35 GMT  
		Size: 12.3 KB (12260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4992ddaf3fbc8a86cae023d8a55729ea8c144f3fd64ce6429f512019224862f`  
		Last Modified: Sat, 16 Mar 2024 03:21:35 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e62fadc79b84d0c222bb06eb7e644dd0ab83db94c3bcc9ebe9067fca5a45b4`  
		Last Modified: Sat, 16 Mar 2024 03:21:34 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:cff878efc147e8d2e5d44d35e648df3d94ec338fc6421add7d218d28e2f36337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:96f6c77c07709a3d5bd835e235273cc673c931519be22ce7fc7e1ac9cb9d319b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71915276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90be9674d59f7c548632114deb86d96b1814a7e3b1efe7afdab747410558d61b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:53:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 07:53:40 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 24 Apr 2024 07:53:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 07:53:51 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Apr 2024 07:53:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Apr 2024 07:53:51 GMT
EXPOSE 8888
# Wed, 24 Apr 2024 07:53:51 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Apr 2024 07:53:51 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 24 Apr 2024 07:53:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 07:53:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520be706950d35ea5e8a6d3289b038934be63cb5ed7dc0adfe502c822c248c6d`  
		Last Modified: Wed, 24 Apr 2024 07:54:54 GMT  
		Size: 5.2 MB (5228344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d206190a9d9ab39d3fe0b30d60c2423e6c2972c800400818684f2193b2c92f5`  
		Last Modified: Wed, 24 Apr 2024 07:55:11 GMT  
		Size: 35.2 MB (35228266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac6c0296c98c70367e5edeb0c04b3e149ccb881367aa1050a4923cfca635ef1`  
		Last Modified: Wed, 24 Apr 2024 07:55:07 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb3cf3503e58f50444e8696d20eb1223f3fe3539685ca2de1fb5813adcaafff`  
		Last Modified: Wed, 24 Apr 2024 07:55:07 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7669f20d3f017b13c835da2e7736f4113669a288a0e3773b1435c876e44f274a`  
		Last Modified: Wed, 24 Apr 2024 07:55:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b99b18c80d1f1a91ffcda6d01fc1e102da0ede7771e4dc7afeee3591fd40ab00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64640752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8e448c13ead4c39b4233d16bf661f76baa83412eb466e13382fad9ff61a045`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:25 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Wed, 24 Apr 2024 04:07:25 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:47:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 04:47:49 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 24 Apr 2024 04:48:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 04:48:01 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Apr 2024 04:48:01 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Apr 2024 04:48:01 GMT
EXPOSE 8888
# Wed, 24 Apr 2024 04:48:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Apr 2024 04:48:02 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 24 Apr 2024 04:48:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 04:48:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b871ba8c2778591f604a672382ac37360b43952a34eb6a05b91baa8a39132a0`  
		Last Modified: Wed, 24 Apr 2024 04:48:53 GMT  
		Size: 4.5 MB (4493435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048e129e94db61beff840eec865569072a5d891bafa56496f675615cb9f06b4a`  
		Last Modified: Wed, 24 Apr 2024 04:49:10 GMT  
		Size: 33.5 MB (33528177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1611f02b2c0f442207d7ee4a156bf66fa255552a3e19c7cbf645ed0c83e078`  
		Last Modified: Wed, 24 Apr 2024 04:49:05 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8aa019799e948c99796e0c8f91bbbf68feeae61068fa36a7233d3025c8bc26`  
		Last Modified: Wed, 24 Apr 2024 04:49:05 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb1672e07cf7fc6a172f4faf7c4b2b29b85becaf9d075ca0caf09f8fd052b1c`  
		Last Modified: Wed, 24 Apr 2024 04:49:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:93a21fd0cf886d03724f40fa7f206a36c3b8ce33db7a012c964c855ff048a244
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68720754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4766feb604fd85b210f245bc7968225376ea93b7ec107a1bb885e3055a66e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 11:12:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 11:12:35 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 24 Apr 2024 11:12:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 11:12:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 24 Apr 2024 11:12:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 24 Apr 2024 11:12:42 GMT
EXPOSE 8888
# Wed, 24 Apr 2024 11:12:42 GMT
VOLUME [/var/lib/chronograf]
# Wed, 24 Apr 2024 11:12:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 24 Apr 2024 11:12:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 11:12:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9970cd3c9ba98c288db4431779cc3c04c36809c5b9099409912a1d0954eafe7`  
		Last Modified: Wed, 24 Apr 2024 11:13:26 GMT  
		Size: 5.2 MB (5210732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e4a1cd79dcbead26f1a4fa4b98707ec8db81712ea765cd1e18dcab1771729f`  
		Last Modified: Wed, 24 Apr 2024 11:13:40 GMT  
		Size: 33.4 MB (33398285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4cd6d69300a0bb070b26147a6db193a3a7913e5958651df0f6ff711960ea79`  
		Last Modified: Wed, 24 Apr 2024 11:13:37 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae1411567fc1c9c3ef4541ab396383fe8d5ad09048636836c33e1b729f35f4`  
		Last Modified: Wed, 24 Apr 2024 11:13:37 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477b95c5e8625010c1cc1ca7c9030edb403c68c9731c23e7c44b4b68a48352d0`  
		Last Modified: Wed, 24 Apr 2024 11:13:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:58038f3e5f95b38efbe31e2dd8c7b7c0da7a926da9b6ee6845699869095111a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c25d48417f45446f783c5adf64c42c1d76444df716f79ea61f71db2172028923
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23361283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cd392d9f55a4830d355e0f9b6d013cadc65691db4951a14030c9261717c704`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:20:06 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 03:20:32 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sat, 16 Mar 2024 03:20:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 03:20:38 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 16 Mar 2024 03:20:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 16 Mar 2024 03:20:38 GMT
EXPOSE 8888
# Sat, 16 Mar 2024 03:20:38 GMT
VOLUME [/var/lib/chronograf]
# Sat, 16 Mar 2024 03:20:38 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 16 Mar 2024 03:20:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 03:20:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98004ffc28465fb13a09790c0b8d8af0ed002fa6fa8a93c0bfc098bb1862afb1`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 284.9 KB (284942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ad7820274585078b0e98dff9ca0a6a138b48fa805200be362ae835e55d935e`  
		Last Modified: Sat, 16 Mar 2024 03:21:38 GMT  
		Size: 19.7 MB (19672268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10615eac7f71b29e6e8a49969cc83939de885312ca46c1b7c853a6986226fc1d`  
		Last Modified: Sat, 16 Mar 2024 03:21:35 GMT  
		Size: 12.3 KB (12260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4992ddaf3fbc8a86cae023d8a55729ea8c144f3fd64ce6429f512019224862f`  
		Last Modified: Sat, 16 Mar 2024 03:21:35 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e62fadc79b84d0c222bb06eb7e644dd0ab83db94c3bcc9ebe9067fca5a45b4`  
		Last Modified: Sat, 16 Mar 2024 03:21:34 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:bc677d048b78b7ee3b2339fea88440e7e1e6f36c322adbceaef16bbd4cdd7c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:e4d3d65dfa3b17d25170a680c6e9bb88c2ffc649a7eea1af1b9512d127f61561
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31590092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1aa448b8cb627fb1b3de3e95e85d1792fb7c84a2324e6bacc6cf6f2bd1c4df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 23 Apr 2024 17:27:49 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates
# Fri, 26 Apr 2024 22:08:23 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 22:08:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf
# Fri, 26 Apr 2024 22:08:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 26 Apr 2024 22:08:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 26 Apr 2024 22:08:29 GMT
EXPOSE 8888
# Fri, 26 Apr 2024 22:08:29 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 22:08:29 GMT
COPY file:1f6f0a0b9c49483e5400adfe0e7eddaca76d6a690f01cf0288b90406e2da965c in /entrypoint.sh 
# Fri, 26 Apr 2024 22:08:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 22:08:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec84f8c4b4c91fcb32de58f4c3ad4f074277a222c69804bc60e3dc52fb9edb0`  
		Last Modified: Sat, 16 Mar 2024 03:21:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9451ab070e66261dde2ccade99194ed606e0d2cfd54f79ada2502c394614520c`  
		Last Modified: Tue, 23 Apr 2024 17:28:34 GMT  
		Size: 295.9 KB (295868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546a8b82c5fb489b1dbf78396994620fdcecfaa11ecaf898cb28c9be6454ba02`  
		Last Modified: Fri, 26 Apr 2024 22:09:15 GMT  
		Size: 27.9 MB (27866936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e91faf745cc56c62ba29f9b761f676feff9fcb6ef2bdd744aa8aa6ea6d9e41`  
		Last Modified: Fri, 26 Apr 2024 22:09:11 GMT  
		Size: 12.3 KB (12266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747ae52b83e8dcb5ec955776e51f45ab29101447a4355ac52c7d95df3bdc4306`  
		Last Modified: Fri, 26 Apr 2024 22:09:10 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0963e152ee8236f28dfafb48dc75f73db4336c8c1303e13071ba6f0052367f4a`  
		Last Modified: Fri, 26 Apr 2024 22:09:11 GMT  
		Size: 292.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:00212cde3ec0e7e03064c97967b652a3ccad715a75272d56b16eeb70414f6152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:392c73fd8092f3be72138161975602b6f411a9231b383ce307a8c53e1b292b87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84462839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df456f2e4a0292d497a44d2682d4e00eeeedaafa6b3464dfb2d8b906f2c87d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:54:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 26 Apr 2024 22:08:10 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 22:08:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 26 Apr 2024 22:08:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 26 Apr 2024 22:08:18 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 26 Apr 2024 22:08:18 GMT
EXPOSE 8888
# Fri, 26 Apr 2024 22:08:18 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 22:08:18 GMT
COPY file:322ec550f2fba037831462da9d81d40f7e6c1c94797662b6e166f5d8d36c5b4e in /entrypoint.sh 
# Fri, 26 Apr 2024 22:08:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 22:08:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f2b6422b4a4d96ef0937dc3f999ca0e9a3d3c511bb569f06dabd00917fb88c`  
		Last Modified: Wed, 24 Apr 2024 07:55:22 GMT  
		Size: 7.9 MB (7873309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd8036513aebcbc1aa0503e1eea934239be55bfba53a905f7e2f330f3eb098b`  
		Last Modified: Fri, 26 Apr 2024 22:09:00 GMT  
		Size: 47.4 MB (47414583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898f59b0daa71b77057c779cd4332f4f21f234f0a7f4d7fb396f0c80607788fa`  
		Last Modified: Fri, 26 Apr 2024 22:08:54 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8dc3abe6e300121116e074d1f11f2ac81cbca3b64b2ada8d39bad1ad88fa3a`  
		Last Modified: Fri, 26 Apr 2024 22:08:54 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a177aec86da3c2e057f5f2b64f712e5d1eb9ce89895689ea7009e03de8d2e97`  
		Last Modified: Fri, 26 Apr 2024 22:08:54 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ff93bd9576060dc03a733fd949b2138b6f22a702812151c683edb1b074c63534
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75744378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e27f95eef0625e76a75f07f71d1e2ec121ada9b126ecd4cb001f8d7fa58164`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:48:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 26 Apr 2024 21:59:12 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Fri, 26 Apr 2024 21:59:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 26 Apr 2024 21:59:28 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 26 Apr 2024 21:59:28 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 26 Apr 2024 21:59:28 GMT
EXPOSE 8888
# Fri, 26 Apr 2024 21:59:29 GMT
VOLUME [/var/lib/chronograf]
# Fri, 26 Apr 2024 21:59:29 GMT
COPY file:322ec550f2fba037831462da9d81d40f7e6c1c94797662b6e166f5d8d36c5b4e in /entrypoint.sh 
# Fri, 26 Apr 2024 21:59:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 21:59:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c215aa1ee7dcb414d32d3379d194e0898aeb361148172b49be795e68955e0e6c`  
		Last Modified: Wed, 24 Apr 2024 04:49:20 GMT  
		Size: 6.5 MB (6497997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6652e0b271a4a516ee18f95969d55d8ff1c5e99fab60cd88381e0f92d47df64`  
		Last Modified: Fri, 26 Apr 2024 21:59:55 GMT  
		Size: 44.5 MB (44481468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd921d46385df6c1e4aeb94f04b6a87469a8734325cf5f4f23f14fc5b4fc4d00`  
		Last Modified: Fri, 26 Apr 2024 21:59:46 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8b8a0ecd7b222ce7c45a000b9fae64800ce777eb742cf4ad017ed41c9a6e98`  
		Last Modified: Fri, 26 Apr 2024 21:59:46 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdea724c673507feacd1f1647b5710a94c0962eb15d34b499fb922e402a0f64e`  
		Last Modified: Fri, 26 Apr 2024 21:59:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ef62f8997e8e2908f40073336f7f3ecae0f2d4b873e5eaccf4a0bf1fd0932bfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82039807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e687daa3d3a56538e9daff12e27a705bfbee3f9f1e53f9a0cf30a89b3fb74fcf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 11:12:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 29 Apr 2024 19:59:09 GMT
ENV CHRONOGRAF_VERSION=1.10.4
# Mon, 29 Apr 2024 19:59:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 29 Apr 2024 19:59:17 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 29 Apr 2024 19:59:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 29 Apr 2024 19:59:17 GMT
EXPOSE 8888
# Mon, 29 Apr 2024 19:59:17 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Apr 2024 19:59:17 GMT
COPY file:322ec550f2fba037831462da9d81d40f7e6c1c94797662b6e166f5d8d36c5b4e in /entrypoint.sh 
# Mon, 29 Apr 2024 19:59:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Apr 2024 19:59:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3777eaa448d12fa64be79faf0defd5c860f34e6f5785fc5e34b07bd082d784e1`  
		Last Modified: Wed, 24 Apr 2024 11:13:49 GMT  
		Size: 7.6 MB (7649956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9ecf2bddea629649f67d6e6b64ef35f9be939d68ec2fbd9ab4551ac08d0b70`  
		Last Modified: Mon, 29 Apr 2024 19:59:37 GMT  
		Size: 45.2 MB (45185447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b736e8a28ad4ff6c1484f1c6c86899d318f86c8ce53512c3b1e7e9cc7c6cca`  
		Last Modified: Mon, 29 Apr 2024 19:59:31 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66938160c27eb30ea21022ebae3accbc0611e3ec21216bfbb79b93995efb0651`  
		Last Modified: Mon, 29 Apr 2024 19:59:32 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e699ac1e7152c5f174ebd82e9650342f1e2d7a79f4ebfa183934588058b6ebb`  
		Last Modified: Mon, 29 Apr 2024 19:59:31 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
