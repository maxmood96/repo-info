<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.6`](#chronograf16)
-	[`chronograf:1.6-alpine`](#chronograf16-alpine)
-	[`chronograf:1.6.2`](#chronograf162)
-	[`chronograf:1.6.2-alpine`](#chronograf162-alpine)
-	[`chronograf:1.7`](#chronograf17)
-	[`chronograf:1.7-alpine`](#chronograf17-alpine)
-	[`chronograf:1.7.17`](#chronograf1717)
-	[`chronograf:1.7.17-alpine`](#chronograf1717-alpine)
-	[`chronograf:1.8`](#chronograf18)
-	[`chronograf:1.8-alpine`](#chronograf18-alpine)
-	[`chronograf:1.8.8`](#chronograf188)
-	[`chronograf:1.8.8-alpine`](#chronograf188-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.6`

```console
$ docker pull chronograf@sha256:a53ba47f101a044ea048c1b4c77877889d3bd590c50e33277ccb7212fee06d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:9122f4e9169c6569429abbd5c8927ae619bb04f4306244f632e7362ed9cd0fde
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49357249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f6e90dfa5e11a4a8f429a02647b041dab04136816d9cb02bb8ee86f4d2866b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 01:46:01 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sat, 10 Apr 2021 01:46:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 10 Apr 2021 01:46:15 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 10 Apr 2021 01:46:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 10 Apr 2021 01:46:16 GMT
EXPOSE 8888
# Sat, 10 Apr 2021 01:46:16 GMT
VOLUME [/var/lib/chronograf]
# Sat, 10 Apr 2021 01:46:17 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 10 Apr 2021 01:46:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 01:46:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b94e8b3cb7869f3c4a6438daab56a93381415beefa0cc91809c790d6fc396c9`  
		Last Modified: Sat, 10 Apr 2021 01:47:37 GMT  
		Size: 6.8 MB (6760279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e517f90a39ab22793e1695fb74e4ebfa2c59b4db2b0b1b4b95333565257bd13`  
		Last Modified: Sat, 10 Apr 2021 01:47:43 GMT  
		Size: 20.0 MB (20044315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d23fa4b4dd704630d501816c1f5bf921f02a7cce760a7e47f48aab8414f838`  
		Last Modified: Sat, 10 Apr 2021 01:47:35 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49922cd643ee8e3097c54fc37017062982e09e2a90bcbc75fad123378f013c56`  
		Last Modified: Sat, 10 Apr 2021 01:47:35 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47dae8db373eb79d57131ec96b42625d9021d4df31ef2c614ce38ba2aaf19fe9`  
		Last Modified: Sat, 10 Apr 2021 01:47:35 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e42b0fff2e2d42ba6e111ba931f60ca6389acedf0b9c42f3c0b1c21eb3928016
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43935906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54065c5adaad961b5bb00faa6e598f35b8912573feed75da263d473d7401691`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 30 Mar 2021 23:12:00 GMT
ADD file:acbde5217c39a55c2b477871bd72f5e796a00ff8fe549861a010b3585acf79c8 in / 
# Tue, 30 Mar 2021 23:12:03 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:14:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 01:14:04 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 31 Mar 2021 01:14:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Mar 2021 01:14:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 31 Mar 2021 01:14:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 31 Mar 2021 01:14:31 GMT
EXPOSE 8888
# Wed, 31 Mar 2021 01:14:32 GMT
VOLUME [/var/lib/chronograf]
# Wed, 31 Mar 2021 01:14:33 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 31 Mar 2021 01:14:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 01:14:37 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6d58e1656f7868d0ecf4058d1f7d9d64560bbd4a5fff5a796f31171993a2da7c`  
		Last Modified: Tue, 30 Mar 2021 23:19:07 GMT  
		Size: 19.3 MB (19315190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede0b41a4840303eba6b7d45fc9aa8f389f9d8bad1151efeee8105b5f31f1b87`  
		Last Modified: Wed, 31 Mar 2021 01:16:51 GMT  
		Size: 5.8 MB (5779533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c192ccd0ad1115b11d078995811ba64fb4c7979a14fbe173cbb5e4416d9f8f9`  
		Last Modified: Wed, 31 Mar 2021 01:16:57 GMT  
		Size: 18.8 MB (18816785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690564442209c922f369f838b27256b304c4b7a8bccdf8cf8eefe074ce843e05`  
		Last Modified: Wed, 31 Mar 2021 01:16:45 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d3b2ce768eaf365858d1e45c9cb00c001f75edc1d67da781bd7ed7643ed49b`  
		Last Modified: Wed, 31 Mar 2021 01:16:45 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae26db92cc7af703f851a41f670a32a00123ff30750666325190befbace9a6fe`  
		Last Modified: Wed, 31 Mar 2021 01:16:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:d3191eb7faadae375d365f5a594017d32e566afeeb023c1a4f6a709f795ed887
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45420059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f2f2f89b3a404575c5b9062c2c2510dc997dfced56d995715674fd4a20dd8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 10 Apr 2021 00:44:13 GMT
ADD file:a74d7856e70f2e18d2509edd9f0527254a69e9d1347715149c772a0d4ca7d509 in / 
# Sat, 10 Apr 2021 00:44:14 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 04:41:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 04:41:07 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sat, 10 Apr 2021 04:41:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 10 Apr 2021 04:41:21 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 10 Apr 2021 04:41:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 10 Apr 2021 04:41:23 GMT
EXPOSE 8888
# Sat, 10 Apr 2021 04:41:24 GMT
VOLUME [/var/lib/chronograf]
# Sat, 10 Apr 2021 04:41:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 10 Apr 2021 04:41:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 04:41:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bc16ed4a30c7b74efb2ba46d7df8a6591a02826832c27a5cf55cc6e06111a5a6`  
		Last Modified: Sat, 10 Apr 2021 00:50:10 GMT  
		Size: 20.4 MB (20389366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c2ed72c66d02fd13b044d79fa58cf56d1a3ddb077cc81ccb643a341ab5eefb`  
		Last Modified: Sat, 10 Apr 2021 04:43:10 GMT  
		Size: 6.0 MB (6047617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6f4f19ee28d52e11b810e3a09831437ee2908f3535e16b27dcc57fbafe7126`  
		Last Modified: Sat, 10 Apr 2021 04:43:14 GMT  
		Size: 19.0 MB (18958681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7275e69769e809ba672eb40634cae4205dbab7eba267fb4877ff3e809f7e52`  
		Last Modified: Sat, 10 Apr 2021 04:43:09 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125a92161fa34fee2ea3421bbf1ab18080fcea571289bbe756f68e010bf402e0`  
		Last Modified: Sat, 10 Apr 2021 04:43:09 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a28ebaace9994955513e1bba4403399ae663e862091004802c9e4db196c0925`  
		Last Modified: Sat, 10 Apr 2021 04:43:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6-alpine`

```console
$ docker pull chronograf@sha256:afc27e51a4f2e0e1c49219d66742fdd469a62c67bc69b58e57ecd83a25fef73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.6-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c30e5d9e5d75dbf5b4175548986cb9ae607ab4537ba2e2d0cc7b9338c9775f33
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14841938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65856dff812d4f4d97e3b878321358057daa1de887ade6822609e016b78151e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:17:19 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 01 Apr 2021 13:33:33 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 01 Apr 2021 13:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 01 Apr 2021 13:33:37 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Thu, 01 Apr 2021 13:33:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 01 Apr 2021 13:33:38 GMT
EXPOSE 8888
# Thu, 01 Apr 2021 13:33:38 GMT
VOLUME [/var/lib/chronograf]
# Thu, 01 Apr 2021 13:33:38 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 01 Apr 2021 13:33:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 13:33:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28ec0c47ed2e19e5d27fab02ef23b68ffd819172e08050fa1da307311f9c707`  
		Last Modified: Wed, 31 Mar 2021 22:18:17 GMT  
		Size: 280.9 KB (280883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc226b3ef375839cadeb2165bafdcee1fb404ea1b27b057083218f4e85cb2a1`  
		Last Modified: Thu, 01 Apr 2021 13:34:34 GMT  
		Size: 11.7 MB (11736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe1217af7ba06ad5746c3902bdb5f510a0625d41959d924f2176119814677cf`  
		Last Modified: Thu, 01 Apr 2021 13:34:32 GMT  
		Size: 12.3 KB (12274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101d057d02e9e0c61a67afc52470b5727406fc5897333d49ae443686fed3a418`  
		Last Modified: Thu, 01 Apr 2021 13:34:31 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9dd9641d9f9c9c37df8ca9feba03e1174a77198e546a2f8ef8542fcd0f01a8`  
		Last Modified: Thu, 01 Apr 2021 13:34:31 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2`

```console
$ docker pull chronograf@sha256:a53ba47f101a044ea048c1b4c77877889d3bd590c50e33277ccb7212fee06d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:9122f4e9169c6569429abbd5c8927ae619bb04f4306244f632e7362ed9cd0fde
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49357249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f6e90dfa5e11a4a8f429a02647b041dab04136816d9cb02bb8ee86f4d2866b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 01:46:01 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sat, 10 Apr 2021 01:46:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 10 Apr 2021 01:46:15 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 10 Apr 2021 01:46:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 10 Apr 2021 01:46:16 GMT
EXPOSE 8888
# Sat, 10 Apr 2021 01:46:16 GMT
VOLUME [/var/lib/chronograf]
# Sat, 10 Apr 2021 01:46:17 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 10 Apr 2021 01:46:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 01:46:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b94e8b3cb7869f3c4a6438daab56a93381415beefa0cc91809c790d6fc396c9`  
		Last Modified: Sat, 10 Apr 2021 01:47:37 GMT  
		Size: 6.8 MB (6760279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e517f90a39ab22793e1695fb74e4ebfa2c59b4db2b0b1b4b95333565257bd13`  
		Last Modified: Sat, 10 Apr 2021 01:47:43 GMT  
		Size: 20.0 MB (20044315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d23fa4b4dd704630d501816c1f5bf921f02a7cce760a7e47f48aab8414f838`  
		Last Modified: Sat, 10 Apr 2021 01:47:35 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49922cd643ee8e3097c54fc37017062982e09e2a90bcbc75fad123378f013c56`  
		Last Modified: Sat, 10 Apr 2021 01:47:35 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47dae8db373eb79d57131ec96b42625d9021d4df31ef2c614ce38ba2aaf19fe9`  
		Last Modified: Sat, 10 Apr 2021 01:47:35 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e42b0fff2e2d42ba6e111ba931f60ca6389acedf0b9c42f3c0b1c21eb3928016
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43935906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54065c5adaad961b5bb00faa6e598f35b8912573feed75da263d473d7401691`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 30 Mar 2021 23:12:00 GMT
ADD file:acbde5217c39a55c2b477871bd72f5e796a00ff8fe549861a010b3585acf79c8 in / 
# Tue, 30 Mar 2021 23:12:03 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:14:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 01:14:04 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 31 Mar 2021 01:14:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Mar 2021 01:14:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 31 Mar 2021 01:14:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 31 Mar 2021 01:14:31 GMT
EXPOSE 8888
# Wed, 31 Mar 2021 01:14:32 GMT
VOLUME [/var/lib/chronograf]
# Wed, 31 Mar 2021 01:14:33 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 31 Mar 2021 01:14:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 01:14:37 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6d58e1656f7868d0ecf4058d1f7d9d64560bbd4a5fff5a796f31171993a2da7c`  
		Last Modified: Tue, 30 Mar 2021 23:19:07 GMT  
		Size: 19.3 MB (19315190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede0b41a4840303eba6b7d45fc9aa8f389f9d8bad1151efeee8105b5f31f1b87`  
		Last Modified: Wed, 31 Mar 2021 01:16:51 GMT  
		Size: 5.8 MB (5779533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c192ccd0ad1115b11d078995811ba64fb4c7979a14fbe173cbb5e4416d9f8f9`  
		Last Modified: Wed, 31 Mar 2021 01:16:57 GMT  
		Size: 18.8 MB (18816785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690564442209c922f369f838b27256b304c4b7a8bccdf8cf8eefe074ce843e05`  
		Last Modified: Wed, 31 Mar 2021 01:16:45 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d3b2ce768eaf365858d1e45c9cb00c001f75edc1d67da781bd7ed7643ed49b`  
		Last Modified: Wed, 31 Mar 2021 01:16:45 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae26db92cc7af703f851a41f670a32a00123ff30750666325190befbace9a6fe`  
		Last Modified: Wed, 31 Mar 2021 01:16:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:d3191eb7faadae375d365f5a594017d32e566afeeb023c1a4f6a709f795ed887
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45420059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f2f2f89b3a404575c5b9062c2c2510dc997dfced56d995715674fd4a20dd8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 10 Apr 2021 00:44:13 GMT
ADD file:a74d7856e70f2e18d2509edd9f0527254a69e9d1347715149c772a0d4ca7d509 in / 
# Sat, 10 Apr 2021 00:44:14 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 04:41:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 04:41:07 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sat, 10 Apr 2021 04:41:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 10 Apr 2021 04:41:21 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 10 Apr 2021 04:41:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 10 Apr 2021 04:41:23 GMT
EXPOSE 8888
# Sat, 10 Apr 2021 04:41:24 GMT
VOLUME [/var/lib/chronograf]
# Sat, 10 Apr 2021 04:41:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 10 Apr 2021 04:41:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 04:41:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bc16ed4a30c7b74efb2ba46d7df8a6591a02826832c27a5cf55cc6e06111a5a6`  
		Last Modified: Sat, 10 Apr 2021 00:50:10 GMT  
		Size: 20.4 MB (20389366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c2ed72c66d02fd13b044d79fa58cf56d1a3ddb077cc81ccb643a341ab5eefb`  
		Last Modified: Sat, 10 Apr 2021 04:43:10 GMT  
		Size: 6.0 MB (6047617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6f4f19ee28d52e11b810e3a09831437ee2908f3535e16b27dcc57fbafe7126`  
		Last Modified: Sat, 10 Apr 2021 04:43:14 GMT  
		Size: 19.0 MB (18958681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7275e69769e809ba672eb40634cae4205dbab7eba267fb4877ff3e809f7e52`  
		Last Modified: Sat, 10 Apr 2021 04:43:09 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125a92161fa34fee2ea3421bbf1ab18080fcea571289bbe756f68e010bf402e0`  
		Last Modified: Sat, 10 Apr 2021 04:43:09 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a28ebaace9994955513e1bba4403399ae663e862091004802c9e4db196c0925`  
		Last Modified: Sat, 10 Apr 2021 04:43:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2-alpine`

```console
$ docker pull chronograf@sha256:afc27e51a4f2e0e1c49219d66742fdd469a62c67bc69b58e57ecd83a25fef73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.6.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c30e5d9e5d75dbf5b4175548986cb9ae607ab4537ba2e2d0cc7b9338c9775f33
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14841938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65856dff812d4f4d97e3b878321358057daa1de887ade6822609e016b78151e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:17:19 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 01 Apr 2021 13:33:33 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 01 Apr 2021 13:33:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 01 Apr 2021 13:33:37 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Thu, 01 Apr 2021 13:33:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 01 Apr 2021 13:33:38 GMT
EXPOSE 8888
# Thu, 01 Apr 2021 13:33:38 GMT
VOLUME [/var/lib/chronograf]
# Thu, 01 Apr 2021 13:33:38 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 01 Apr 2021 13:33:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 13:33:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28ec0c47ed2e19e5d27fab02ef23b68ffd819172e08050fa1da307311f9c707`  
		Last Modified: Wed, 31 Mar 2021 22:18:17 GMT  
		Size: 280.9 KB (280883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc226b3ef375839cadeb2165bafdcee1fb404ea1b27b057083218f4e85cb2a1`  
		Last Modified: Thu, 01 Apr 2021 13:34:34 GMT  
		Size: 11.7 MB (11736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe1217af7ba06ad5746c3902bdb5f510a0625d41959d924f2176119814677cf`  
		Last Modified: Thu, 01 Apr 2021 13:34:32 GMT  
		Size: 12.3 KB (12274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101d057d02e9e0c61a67afc52470b5727406fc5897333d49ae443686fed3a418`  
		Last Modified: Thu, 01 Apr 2021 13:34:31 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9dd9641d9f9c9c37df8ca9feba03e1174a77198e546a2f8ef8542fcd0f01a8`  
		Last Modified: Thu, 01 Apr 2021 13:34:31 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:f6504a533df68beae2227ca0a899ec3ad448cb545381495ce78648aafde3ce04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:c868a2c7f0181695af3b718a006faa43db0063a9b12515ff7ad096059b8adafe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65375504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dee4b21ef76faf35b5c6d3806469acff9a4a59f30290797b0a07c395df0eee0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 01:46:36 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 10 Apr 2021 01:46:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 10 Apr 2021 01:46:48 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 10 Apr 2021 01:46:48 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 10 Apr 2021 01:46:48 GMT
EXPOSE 8888
# Sat, 10 Apr 2021 01:46:48 GMT
VOLUME [/var/lib/chronograf]
# Sat, 10 Apr 2021 01:46:48 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 10 Apr 2021 01:46:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 01:46:49 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300ad877774ce0dd9f8566b2b6692a4514eac2b0742a7a7fee73d6bdeb8c5b41`  
		Last Modified: Sat, 10 Apr 2021 01:47:56 GMT  
		Size: 4.5 MB (4506035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdf0db69b1b4b253b99a380920e8f6fbdae800a8ff2ca9984a23c819142d564`  
		Last Modified: Sat, 10 Apr 2021 01:48:01 GMT  
		Size: 38.3 MB (38316810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e987c2aba8cacb9ded8e1620382b90b0176950d4bbc73de0b533c0c9364d43`  
		Last Modified: Sat, 10 Apr 2021 01:47:55 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c50be0df49fca023a939ed1e3c3eff1572c465a3bc7e768f09cbb3a97db9faf`  
		Last Modified: Sat, 10 Apr 2021 01:47:55 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f720e22c9a6a4d88e4f1a83d053eb9276a6ba80aa8b5deb7c2f3ed355a193c30`  
		Last Modified: Sat, 10 Apr 2021 01:47:55 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:31e2bf930f396491d12148a4b17bdc489df718739ba1e397b1f7d99cb609f6c5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58993626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c545611d03e5de37fffb8ad02a523a861e6185e2b4b4e9d2be5b2f3e4072967`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 30 Mar 2021 23:12:00 GMT
ADD file:acbde5217c39a55c2b477871bd72f5e796a00ff8fe549861a010b3585acf79c8 in / 
# Tue, 30 Mar 2021 23:12:03 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:15:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 01:15:03 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 31 Mar 2021 01:15:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Mar 2021 01:15:32 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 31 Mar 2021 01:15:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 31 Mar 2021 01:15:34 GMT
EXPOSE 8888
# Wed, 31 Mar 2021 01:15:36 GMT
VOLUME [/var/lib/chronograf]
# Wed, 31 Mar 2021 01:15:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 31 Mar 2021 01:15:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 01:15:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6d58e1656f7868d0ecf4058d1f7d9d64560bbd4a5fff5a796f31171993a2da7c`  
		Last Modified: Tue, 30 Mar 2021 23:19:07 GMT  
		Size: 19.3 MB (19315190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68e7bd81163525bf11666e5d5f59d376bcd3a7d1ed969e4d54e181903b1e117`  
		Last Modified: Wed, 31 Mar 2021 01:17:05 GMT  
		Size: 3.9 MB (3879587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4535d706a6af03339c01164fd75aba81217861e04fe2202f635c2db518164d8`  
		Last Modified: Wed, 31 Mar 2021 01:17:15 GMT  
		Size: 35.8 MB (35774464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a568137931e0eb08d625fd2b2b9ba14649c46df89ff9f6e1644376a7c3c164`  
		Last Modified: Wed, 31 Mar 2021 01:17:05 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffae872c254022f4500fc86a160dde6acf113c76cd4de6835e126fc9add7e2d4`  
		Last Modified: Wed, 31 Mar 2021 01:17:04 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c688e6069a50dfe7bbd8ed4370ba281303ba15f4b4ccb00da7172ac2a5471f97`  
		Last Modified: Wed, 31 Mar 2021 01:17:04 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a834131967da404cc71c128f5588223db46014e88207980f8a70d95692994b05
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60477273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f206c3cb12e4eea6ce76e3cb530cbd39460e430484eae46ddd13fdaebd5c5d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 10 Apr 2021 00:44:13 GMT
ADD file:a74d7856e70f2e18d2509edd9f0527254a69e9d1347715149c772a0d4ca7d509 in / 
# Sat, 10 Apr 2021 00:44:14 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 04:41:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 04:41:51 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 10 Apr 2021 04:42:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 10 Apr 2021 04:42:11 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 10 Apr 2021 04:42:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 10 Apr 2021 04:42:13 GMT
EXPOSE 8888
# Sat, 10 Apr 2021 04:42:15 GMT
VOLUME [/var/lib/chronograf]
# Sat, 10 Apr 2021 04:42:16 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 10 Apr 2021 04:42:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 04:42:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bc16ed4a30c7b74efb2ba46d7df8a6591a02826832c27a5cf55cc6e06111a5a6`  
		Last Modified: Sat, 10 Apr 2021 00:50:10 GMT  
		Size: 20.4 MB (20389366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0de3bce265e7a00be94e9fafbf56345070c36fcaabcc462b6646373faaef4b4`  
		Last Modified: Sat, 10 Apr 2021 04:43:21 GMT  
		Size: 4.1 MB (4082312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353e13b8c1127ef8ce287a777641f8718cb8b8cd484ce3ca4509b098cca9bb83`  
		Last Modified: Sat, 10 Apr 2021 04:43:28 GMT  
		Size: 36.0 MB (35981191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d67d15d7dd2207c4b1d19dc5ed875c2622401280463192fb8fc525fa760f09`  
		Last Modified: Sat, 10 Apr 2021 04:43:20 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00d84f3c99b9e1d7f0c7e6dbdc8b6e9dacc49a6ad7adc97c586c794d9b951fd`  
		Last Modified: Sat, 10 Apr 2021 04:43:20 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d375f68cbaf00b6da2bd808f4fdc80e36ca97deddc6de80cb157aaa0dab973f9`  
		Last Modified: Sat, 10 Apr 2021 04:43:20 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:35bb95c2ed1e819228f870749b9c01b97d58227f545933f6cad7b149a77431ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:24d631d94c64a0bd07088255cda6b0c80cfe89bd6c343488b6f635a4e35f2c43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22660393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec776de9bb4889f586e609a2dd7e5a88af29e7cd9ae866357b1b7db46c5c463d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:17:19 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 01 Apr 2021 13:33:45 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 01 Apr 2021 13:33:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 01 Apr 2021 13:33:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 01 Apr 2021 13:33:50 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 01 Apr 2021 13:33:50 GMT
EXPOSE 8888
# Thu, 01 Apr 2021 13:33:50 GMT
VOLUME [/var/lib/chronograf]
# Thu, 01 Apr 2021 13:33:51 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 01 Apr 2021 13:33:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 13:33:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28ec0c47ed2e19e5d27fab02ef23b68ffd819172e08050fa1da307311f9c707`  
		Last Modified: Wed, 31 Mar 2021 22:18:17 GMT  
		Size: 280.9 KB (280883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b93abd0f45a22322f35068b2d14f356137c237350ddbbee82fd3332bbfe618`  
		Last Modified: Thu, 01 Apr 2021 13:34:53 GMT  
		Size: 19.6 MB (19555245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5aa73c58e233eccfc6a5db938c48576a8845cf57ebb3cb2eff4a091031b519`  
		Last Modified: Thu, 01 Apr 2021 13:34:48 GMT  
		Size: 12.3 KB (12262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42db2f0aa6f62d623761ae0d9cc1236d3a12d4bfd20e21a72ccc5e3372178b9f`  
		Last Modified: Thu, 01 Apr 2021 13:34:48 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699eae2537b73fba217cb8ea11c313d0f8c380ef42fce9689bf884eece8f69bd`  
		Last Modified: Thu, 01 Apr 2021 13:34:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:f6504a533df68beae2227ca0a899ec3ad448cb545381495ce78648aafde3ce04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:c868a2c7f0181695af3b718a006faa43db0063a9b12515ff7ad096059b8adafe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65375504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dee4b21ef76faf35b5c6d3806469acff9a4a59f30290797b0a07c395df0eee0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 01:46:36 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 10 Apr 2021 01:46:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 10 Apr 2021 01:46:48 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 10 Apr 2021 01:46:48 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 10 Apr 2021 01:46:48 GMT
EXPOSE 8888
# Sat, 10 Apr 2021 01:46:48 GMT
VOLUME [/var/lib/chronograf]
# Sat, 10 Apr 2021 01:46:48 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 10 Apr 2021 01:46:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 01:46:49 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300ad877774ce0dd9f8566b2b6692a4514eac2b0742a7a7fee73d6bdeb8c5b41`  
		Last Modified: Sat, 10 Apr 2021 01:47:56 GMT  
		Size: 4.5 MB (4506035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdf0db69b1b4b253b99a380920e8f6fbdae800a8ff2ca9984a23c819142d564`  
		Last Modified: Sat, 10 Apr 2021 01:48:01 GMT  
		Size: 38.3 MB (38316810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e987c2aba8cacb9ded8e1620382b90b0176950d4bbc73de0b533c0c9364d43`  
		Last Modified: Sat, 10 Apr 2021 01:47:55 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c50be0df49fca023a939ed1e3c3eff1572c465a3bc7e768f09cbb3a97db9faf`  
		Last Modified: Sat, 10 Apr 2021 01:47:55 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f720e22c9a6a4d88e4f1a83d053eb9276a6ba80aa8b5deb7c2f3ed355a193c30`  
		Last Modified: Sat, 10 Apr 2021 01:47:55 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:31e2bf930f396491d12148a4b17bdc489df718739ba1e397b1f7d99cb609f6c5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58993626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c545611d03e5de37fffb8ad02a523a861e6185e2b4b4e9d2be5b2f3e4072967`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 30 Mar 2021 23:12:00 GMT
ADD file:acbde5217c39a55c2b477871bd72f5e796a00ff8fe549861a010b3585acf79c8 in / 
# Tue, 30 Mar 2021 23:12:03 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:15:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 01:15:03 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 31 Mar 2021 01:15:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Mar 2021 01:15:32 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 31 Mar 2021 01:15:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 31 Mar 2021 01:15:34 GMT
EXPOSE 8888
# Wed, 31 Mar 2021 01:15:36 GMT
VOLUME [/var/lib/chronograf]
# Wed, 31 Mar 2021 01:15:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 31 Mar 2021 01:15:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 01:15:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6d58e1656f7868d0ecf4058d1f7d9d64560bbd4a5fff5a796f31171993a2da7c`  
		Last Modified: Tue, 30 Mar 2021 23:19:07 GMT  
		Size: 19.3 MB (19315190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68e7bd81163525bf11666e5d5f59d376bcd3a7d1ed969e4d54e181903b1e117`  
		Last Modified: Wed, 31 Mar 2021 01:17:05 GMT  
		Size: 3.9 MB (3879587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4535d706a6af03339c01164fd75aba81217861e04fe2202f635c2db518164d8`  
		Last Modified: Wed, 31 Mar 2021 01:17:15 GMT  
		Size: 35.8 MB (35774464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a568137931e0eb08d625fd2b2b9ba14649c46df89ff9f6e1644376a7c3c164`  
		Last Modified: Wed, 31 Mar 2021 01:17:05 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffae872c254022f4500fc86a160dde6acf113c76cd4de6835e126fc9add7e2d4`  
		Last Modified: Wed, 31 Mar 2021 01:17:04 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c688e6069a50dfe7bbd8ed4370ba281303ba15f4b4ccb00da7172ac2a5471f97`  
		Last Modified: Wed, 31 Mar 2021 01:17:04 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a834131967da404cc71c128f5588223db46014e88207980f8a70d95692994b05
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60477273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f206c3cb12e4eea6ce76e3cb530cbd39460e430484eae46ddd13fdaebd5c5d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 10 Apr 2021 00:44:13 GMT
ADD file:a74d7856e70f2e18d2509edd9f0527254a69e9d1347715149c772a0d4ca7d509 in / 
# Sat, 10 Apr 2021 00:44:14 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 04:41:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 04:41:51 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 10 Apr 2021 04:42:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 10 Apr 2021 04:42:11 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 10 Apr 2021 04:42:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 10 Apr 2021 04:42:13 GMT
EXPOSE 8888
# Sat, 10 Apr 2021 04:42:15 GMT
VOLUME [/var/lib/chronograf]
# Sat, 10 Apr 2021 04:42:16 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 10 Apr 2021 04:42:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 04:42:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bc16ed4a30c7b74efb2ba46d7df8a6591a02826832c27a5cf55cc6e06111a5a6`  
		Last Modified: Sat, 10 Apr 2021 00:50:10 GMT  
		Size: 20.4 MB (20389366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0de3bce265e7a00be94e9fafbf56345070c36fcaabcc462b6646373faaef4b4`  
		Last Modified: Sat, 10 Apr 2021 04:43:21 GMT  
		Size: 4.1 MB (4082312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353e13b8c1127ef8ce287a777641f8718cb8b8cd484ce3ca4509b098cca9bb83`  
		Last Modified: Sat, 10 Apr 2021 04:43:28 GMT  
		Size: 36.0 MB (35981191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d67d15d7dd2207c4b1d19dc5ed875c2622401280463192fb8fc525fa760f09`  
		Last Modified: Sat, 10 Apr 2021 04:43:20 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00d84f3c99b9e1d7f0c7e6dbdc8b6e9dacc49a6ad7adc97c586c794d9b951fd`  
		Last Modified: Sat, 10 Apr 2021 04:43:20 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d375f68cbaf00b6da2bd808f4fdc80e36ca97deddc6de80cb157aaa0dab973f9`  
		Last Modified: Sat, 10 Apr 2021 04:43:20 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:35bb95c2ed1e819228f870749b9c01b97d58227f545933f6cad7b149a77431ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:24d631d94c64a0bd07088255cda6b0c80cfe89bd6c343488b6f635a4e35f2c43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22660393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec776de9bb4889f586e609a2dd7e5a88af29e7cd9ae866357b1b7db46c5c463d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:17:19 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 01 Apr 2021 13:33:45 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 01 Apr 2021 13:33:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 01 Apr 2021 13:33:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 01 Apr 2021 13:33:50 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 01 Apr 2021 13:33:50 GMT
EXPOSE 8888
# Thu, 01 Apr 2021 13:33:50 GMT
VOLUME [/var/lib/chronograf]
# Thu, 01 Apr 2021 13:33:51 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 01 Apr 2021 13:33:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 13:33:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28ec0c47ed2e19e5d27fab02ef23b68ffd819172e08050fa1da307311f9c707`  
		Last Modified: Wed, 31 Mar 2021 22:18:17 GMT  
		Size: 280.9 KB (280883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b93abd0f45a22322f35068b2d14f356137c237350ddbbee82fd3332bbfe618`  
		Last Modified: Thu, 01 Apr 2021 13:34:53 GMT  
		Size: 19.6 MB (19555245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5aa73c58e233eccfc6a5db938c48576a8845cf57ebb3cb2eff4a091031b519`  
		Last Modified: Thu, 01 Apr 2021 13:34:48 GMT  
		Size: 12.3 KB (12262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42db2f0aa6f62d623761ae0d9cc1236d3a12d4bfd20e21a72ccc5e3372178b9f`  
		Last Modified: Thu, 01 Apr 2021 13:34:48 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699eae2537b73fba217cb8ea11c313d0f8c380ef42fce9689bf884eece8f69bd`  
		Last Modified: Thu, 01 Apr 2021 13:34:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:cd5d982a54351e48fba0be1ee359e6c9e2de09985589c37d50e59416601e19a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:827973fbde254210e229c98b28c49bfaa836e0370c12eabce05672d031ca898f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70442524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c19813229c2a47fd783d48867c427f6430e1cbe1296e3829f1006db744f8a9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 01:46:59 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Sat, 10 Apr 2021 01:47:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 10 Apr 2021 01:47:07 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 10 Apr 2021 01:47:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 10 Apr 2021 01:47:07 GMT
EXPOSE 8888
# Sat, 10 Apr 2021 01:47:07 GMT
VOLUME [/var/lib/chronograf]
# Sat, 10 Apr 2021 01:47:07 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 10 Apr 2021 01:47:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 01:47:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b94e8b3cb7869f3c4a6438daab56a93381415beefa0cc91809c790d6fc396c9`  
		Last Modified: Sat, 10 Apr 2021 01:47:37 GMT  
		Size: 6.8 MB (6760279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770476205d15db72f48832a617c7fa91892ddccb7c3422be4ab97217a764eda8`  
		Last Modified: Sat, 10 Apr 2021 01:48:19 GMT  
		Size: 41.1 MB (41129581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125b6df1d4df29bef6ce3cee1d998fee3fad399c011f2a8afa4a0d5988d905f5`  
		Last Modified: Sat, 10 Apr 2021 01:48:13 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8e1406a19b23d67f40ca2d0066eb881d7c4e10b033dc6f9d8ba8a768a9a440`  
		Last Modified: Sat, 10 Apr 2021 01:48:13 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f93306a56a0605857f00b030fc4d3bded137a1c737c7c37716261e2c820cbe`  
		Last Modified: Sat, 10 Apr 2021 01:48:13 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f8aa43f5c6262d54ec3a88a9994814ee8e19c553bf47b4d64c0d520e32ce093e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63853612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c2c0f6a94429ec2396379b78b5defdbfe9fd92ce93cd455897b7c5a8ec82d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 30 Mar 2021 23:12:00 GMT
ADD file:acbde5217c39a55c2b477871bd72f5e796a00ff8fe549861a010b3585acf79c8 in / 
# Tue, 30 Mar 2021 23:12:03 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:14:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 01:15:55 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Wed, 31 Mar 2021 01:16:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Mar 2021 01:16:20 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 31 Mar 2021 01:16:21 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 31 Mar 2021 01:16:22 GMT
EXPOSE 8888
# Wed, 31 Mar 2021 01:16:23 GMT
VOLUME [/var/lib/chronograf]
# Wed, 31 Mar 2021 01:16:24 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 31 Mar 2021 01:16:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 01:16:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6d58e1656f7868d0ecf4058d1f7d9d64560bbd4a5fff5a796f31171993a2da7c`  
		Last Modified: Tue, 30 Mar 2021 23:19:07 GMT  
		Size: 19.3 MB (19315190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede0b41a4840303eba6b7d45fc9aa8f389f9d8bad1151efeee8105b5f31f1b87`  
		Last Modified: Wed, 31 Mar 2021 01:16:51 GMT  
		Size: 5.8 MB (5779533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9514ec8c6a361715f3d7bb406fac5a8fe1c1b9a530780910ce458786fcb88d8`  
		Last Modified: Wed, 31 Mar 2021 01:17:33 GMT  
		Size: 38.7 MB (38734503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cf0bc57fd7f7bd7904255b04d9f05050164e57f2a03133a3fe53fadc5537f2`  
		Last Modified: Wed, 31 Mar 2021 01:17:23 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d328e23b7fe876fc5619166bf24fc6b870c14eaf2fb8d25b45d99602ad34cd17`  
		Last Modified: Wed, 31 Mar 2021 01:17:23 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f649a222fb0398e59bb1aeaa750dd8e69f27d20d1fb9766b1294a35cebfc11`  
		Last Modified: Wed, 31 Mar 2021 01:17:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:297b60973cd19e3cec05927c378b8c135bc913b235344c3b11aae1f2a8ed0d70
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f449b1271fccdbf7c501e4ce3a667a3842f21d3c1c748cb7c5a21a5686d0f497`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 10 Apr 2021 00:44:13 GMT
ADD file:a74d7856e70f2e18d2509edd9f0527254a69e9d1347715149c772a0d4ca7d509 in / 
# Sat, 10 Apr 2021 00:44:14 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 04:41:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 04:42:32 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Sat, 10 Apr 2021 04:42:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 10 Apr 2021 04:42:47 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 10 Apr 2021 04:42:48 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 10 Apr 2021 04:42:49 GMT
EXPOSE 8888
# Sat, 10 Apr 2021 04:42:50 GMT
VOLUME [/var/lib/chronograf]
# Sat, 10 Apr 2021 04:42:51 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 10 Apr 2021 04:42:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 04:42:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bc16ed4a30c7b74efb2ba46d7df8a6591a02826832c27a5cf55cc6e06111a5a6`  
		Last Modified: Sat, 10 Apr 2021 00:50:10 GMT  
		Size: 20.4 MB (20389366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c2ed72c66d02fd13b044d79fa58cf56d1a3ddb077cc81ccb643a341ab5eefb`  
		Last Modified: Sat, 10 Apr 2021 04:43:10 GMT  
		Size: 6.0 MB (6047617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24621004be61fb6cba386ce3e9263e0e426dff011731b0bb3118b4f0ad2c77ab`  
		Last Modified: Sat, 10 Apr 2021 04:43:52 GMT  
		Size: 38.5 MB (38502575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44434b3f85737bee2cce5ad3210338b916939a731119a5f6d66909e08196d01b`  
		Last Modified: Sat, 10 Apr 2021 04:43:40 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce8f3bdd5d029914779cae6b9dced855ae005ba2e884d7f86ecd3a633d1585d`  
		Last Modified: Sat, 10 Apr 2021 04:43:38 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c68e1532f0d9960688485eead7f17a36d5e44877ce90ac62c73dc217e2f68d`  
		Last Modified: Sat, 10 Apr 2021 04:43:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:32581b9c7942291322f71995d0f7cf2fe16af026dea5d30e59aa5519752d38a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:93b30530319fd27a77ecef88d9c5c920a7e549643a300f24670dd05d1a1c4f41
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25350795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d21d9dab635cb33064bc93cea8cddade8fb2b65a722d836a7a43d4c8f97643`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:17:19 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 01 Apr 2021 13:33:57 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Thu, 01 Apr 2021 13:34:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 01 Apr 2021 13:34:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 01 Apr 2021 13:34:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 01 Apr 2021 13:34:07 GMT
EXPOSE 8888
# Thu, 01 Apr 2021 13:34:07 GMT
VOLUME [/var/lib/chronograf]
# Thu, 01 Apr 2021 13:34:07 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 01 Apr 2021 13:34:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 13:34:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28ec0c47ed2e19e5d27fab02ef23b68ffd819172e08050fa1da307311f9c707`  
		Last Modified: Wed, 31 Mar 2021 22:18:17 GMT  
		Size: 280.9 KB (280883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6b9f165f4bdd3f21be30f28578343a65c63e0817fdb73b574c2fa83e2028fc`  
		Last Modified: Thu, 01 Apr 2021 13:35:11 GMT  
		Size: 22.2 MB (22245645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0350481f214ad36651d1ea1fb25e58e4e80c0cb4c5c6adf0cdc98dc70636ca9`  
		Last Modified: Thu, 01 Apr 2021 13:35:06 GMT  
		Size: 12.3 KB (12266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8005335f5454a8a550fc208952bd9cef9d1345c78e4bec1498895d290711771`  
		Last Modified: Thu, 01 Apr 2021 13:35:06 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cbedf48918106de8db9c17064a34d3f550861f043c93a94e424f41115f302b`  
		Last Modified: Thu, 01 Apr 2021 13:35:06 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.8`

```console
$ docker pull chronograf@sha256:cd5d982a54351e48fba0be1ee359e6c9e2de09985589c37d50e59416601e19a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.8` - linux; amd64

```console
$ docker pull chronograf@sha256:827973fbde254210e229c98b28c49bfaa836e0370c12eabce05672d031ca898f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70442524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c19813229c2a47fd783d48867c427f6430e1cbe1296e3829f1006db744f8a9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 01:46:59 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Sat, 10 Apr 2021 01:47:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 10 Apr 2021 01:47:07 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 10 Apr 2021 01:47:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 10 Apr 2021 01:47:07 GMT
EXPOSE 8888
# Sat, 10 Apr 2021 01:47:07 GMT
VOLUME [/var/lib/chronograf]
# Sat, 10 Apr 2021 01:47:07 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 10 Apr 2021 01:47:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 01:47:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b94e8b3cb7869f3c4a6438daab56a93381415beefa0cc91809c790d6fc396c9`  
		Last Modified: Sat, 10 Apr 2021 01:47:37 GMT  
		Size: 6.8 MB (6760279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770476205d15db72f48832a617c7fa91892ddccb7c3422be4ab97217a764eda8`  
		Last Modified: Sat, 10 Apr 2021 01:48:19 GMT  
		Size: 41.1 MB (41129581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125b6df1d4df29bef6ce3cee1d998fee3fad399c011f2a8afa4a0d5988d905f5`  
		Last Modified: Sat, 10 Apr 2021 01:48:13 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8e1406a19b23d67f40ca2d0066eb881d7c4e10b033dc6f9d8ba8a768a9a440`  
		Last Modified: Sat, 10 Apr 2021 01:48:13 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f93306a56a0605857f00b030fc4d3bded137a1c737c7c37716261e2c820cbe`  
		Last Modified: Sat, 10 Apr 2021 01:48:13 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f8aa43f5c6262d54ec3a88a9994814ee8e19c553bf47b4d64c0d520e32ce093e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63853612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c2c0f6a94429ec2396379b78b5defdbfe9fd92ce93cd455897b7c5a8ec82d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 30 Mar 2021 23:12:00 GMT
ADD file:acbde5217c39a55c2b477871bd72f5e796a00ff8fe549861a010b3585acf79c8 in / 
# Tue, 30 Mar 2021 23:12:03 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:14:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 01:15:55 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Wed, 31 Mar 2021 01:16:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Mar 2021 01:16:20 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 31 Mar 2021 01:16:21 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 31 Mar 2021 01:16:22 GMT
EXPOSE 8888
# Wed, 31 Mar 2021 01:16:23 GMT
VOLUME [/var/lib/chronograf]
# Wed, 31 Mar 2021 01:16:24 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 31 Mar 2021 01:16:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 01:16:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6d58e1656f7868d0ecf4058d1f7d9d64560bbd4a5fff5a796f31171993a2da7c`  
		Last Modified: Tue, 30 Mar 2021 23:19:07 GMT  
		Size: 19.3 MB (19315190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede0b41a4840303eba6b7d45fc9aa8f389f9d8bad1151efeee8105b5f31f1b87`  
		Last Modified: Wed, 31 Mar 2021 01:16:51 GMT  
		Size: 5.8 MB (5779533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9514ec8c6a361715f3d7bb406fac5a8fe1c1b9a530780910ce458786fcb88d8`  
		Last Modified: Wed, 31 Mar 2021 01:17:33 GMT  
		Size: 38.7 MB (38734503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cf0bc57fd7f7bd7904255b04d9f05050164e57f2a03133a3fe53fadc5537f2`  
		Last Modified: Wed, 31 Mar 2021 01:17:23 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d328e23b7fe876fc5619166bf24fc6b870c14eaf2fb8d25b45d99602ad34cd17`  
		Last Modified: Wed, 31 Mar 2021 01:17:23 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f649a222fb0398e59bb1aeaa750dd8e69f27d20d1fb9766b1294a35cebfc11`  
		Last Modified: Wed, 31 Mar 2021 01:17:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:297b60973cd19e3cec05927c378b8c135bc913b235344c3b11aae1f2a8ed0d70
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f449b1271fccdbf7c501e4ce3a667a3842f21d3c1c748cb7c5a21a5686d0f497`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 10 Apr 2021 00:44:13 GMT
ADD file:a74d7856e70f2e18d2509edd9f0527254a69e9d1347715149c772a0d4ca7d509 in / 
# Sat, 10 Apr 2021 00:44:14 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 04:41:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 04:42:32 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Sat, 10 Apr 2021 04:42:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 10 Apr 2021 04:42:47 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 10 Apr 2021 04:42:48 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 10 Apr 2021 04:42:49 GMT
EXPOSE 8888
# Sat, 10 Apr 2021 04:42:50 GMT
VOLUME [/var/lib/chronograf]
# Sat, 10 Apr 2021 04:42:51 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 10 Apr 2021 04:42:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 04:42:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bc16ed4a30c7b74efb2ba46d7df8a6591a02826832c27a5cf55cc6e06111a5a6`  
		Last Modified: Sat, 10 Apr 2021 00:50:10 GMT  
		Size: 20.4 MB (20389366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c2ed72c66d02fd13b044d79fa58cf56d1a3ddb077cc81ccb643a341ab5eefb`  
		Last Modified: Sat, 10 Apr 2021 04:43:10 GMT  
		Size: 6.0 MB (6047617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24621004be61fb6cba386ce3e9263e0e426dff011731b0bb3118b4f0ad2c77ab`  
		Last Modified: Sat, 10 Apr 2021 04:43:52 GMT  
		Size: 38.5 MB (38502575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44434b3f85737bee2cce5ad3210338b916939a731119a5f6d66909e08196d01b`  
		Last Modified: Sat, 10 Apr 2021 04:43:40 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce8f3bdd5d029914779cae6b9dced855ae005ba2e884d7f86ecd3a633d1585d`  
		Last Modified: Sat, 10 Apr 2021 04:43:38 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c68e1532f0d9960688485eead7f17a36d5e44877ce90ac62c73dc217e2f68d`  
		Last Modified: Sat, 10 Apr 2021 04:43:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.8-alpine`

```console
$ docker pull chronograf@sha256:32581b9c7942291322f71995d0f7cf2fe16af026dea5d30e59aa5519752d38a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.8.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:93b30530319fd27a77ecef88d9c5c920a7e549643a300f24670dd05d1a1c4f41
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25350795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d21d9dab635cb33064bc93cea8cddade8fb2b65a722d836a7a43d4c8f97643`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:17:19 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 01 Apr 2021 13:33:57 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Thu, 01 Apr 2021 13:34:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 01 Apr 2021 13:34:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 01 Apr 2021 13:34:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 01 Apr 2021 13:34:07 GMT
EXPOSE 8888
# Thu, 01 Apr 2021 13:34:07 GMT
VOLUME [/var/lib/chronograf]
# Thu, 01 Apr 2021 13:34:07 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 01 Apr 2021 13:34:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 13:34:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28ec0c47ed2e19e5d27fab02ef23b68ffd819172e08050fa1da307311f9c707`  
		Last Modified: Wed, 31 Mar 2021 22:18:17 GMT  
		Size: 280.9 KB (280883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6b9f165f4bdd3f21be30f28578343a65c63e0817fdb73b574c2fa83e2028fc`  
		Last Modified: Thu, 01 Apr 2021 13:35:11 GMT  
		Size: 22.2 MB (22245645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0350481f214ad36651d1ea1fb25e58e4e80c0cb4c5c6adf0cdc98dc70636ca9`  
		Last Modified: Thu, 01 Apr 2021 13:35:06 GMT  
		Size: 12.3 KB (12266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8005335f5454a8a550fc208952bd9cef9d1345c78e4bec1498895d290711771`  
		Last Modified: Thu, 01 Apr 2021 13:35:06 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cbedf48918106de8db9c17064a34d3f550861f043c93a94e424f41115f302b`  
		Last Modified: Thu, 01 Apr 2021 13:35:06 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:32581b9c7942291322f71995d0f7cf2fe16af026dea5d30e59aa5519752d38a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:93b30530319fd27a77ecef88d9c5c920a7e549643a300f24670dd05d1a1c4f41
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25350795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d21d9dab635cb33064bc93cea8cddade8fb2b65a722d836a7a43d4c8f97643`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:13 GMT
ADD file:f77db8e5b937d8ebb7e254eccd4d311798ea9f4dd5081ea2a7e2b1d3790300c2 in / 
# Wed, 31 Mar 2021 20:10:13 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 22:08:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 31 Mar 2021 22:17:19 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 01 Apr 2021 13:33:57 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Thu, 01 Apr 2021 13:34:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 01 Apr 2021 13:34:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 01 Apr 2021 13:34:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 01 Apr 2021 13:34:07 GMT
EXPOSE 8888
# Thu, 01 Apr 2021 13:34:07 GMT
VOLUME [/var/lib/chronograf]
# Thu, 01 Apr 2021 13:34:07 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Thu, 01 Apr 2021 13:34:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 13:34:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:532819f3e44cebad88c82f5393801acb876b7a61d36b84bce646561789bb2018`  
		Last Modified: Wed, 31 Mar 2021 20:11:03 GMT  
		Size: 2.8 MB (2799712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38a141eb441d0521693dd710eb5a2a3ceae66767667e8820f152011f8f8a1de`  
		Last Modified: Wed, 31 Mar 2021 22:12:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28ec0c47ed2e19e5d27fab02ef23b68ffd819172e08050fa1da307311f9c707`  
		Last Modified: Wed, 31 Mar 2021 22:18:17 GMT  
		Size: 280.9 KB (280883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6b9f165f4bdd3f21be30f28578343a65c63e0817fdb73b574c2fa83e2028fc`  
		Last Modified: Thu, 01 Apr 2021 13:35:11 GMT  
		Size: 22.2 MB (22245645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0350481f214ad36651d1ea1fb25e58e4e80c0cb4c5c6adf0cdc98dc70636ca9`  
		Last Modified: Thu, 01 Apr 2021 13:35:06 GMT  
		Size: 12.3 KB (12266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8005335f5454a8a550fc208952bd9cef9d1345c78e4bec1498895d290711771`  
		Last Modified: Thu, 01 Apr 2021 13:35:06 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cbedf48918106de8db9c17064a34d3f550861f043c93a94e424f41115f302b`  
		Last Modified: Thu, 01 Apr 2021 13:35:06 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:cd5d982a54351e48fba0be1ee359e6c9e2de09985589c37d50e59416601e19a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:827973fbde254210e229c98b28c49bfaa836e0370c12eabce05672d031ca898f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70442524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c19813229c2a47fd783d48867c427f6430e1cbe1296e3829f1006db744f8a9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 01:46:59 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Sat, 10 Apr 2021 01:47:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 10 Apr 2021 01:47:07 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 10 Apr 2021 01:47:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 10 Apr 2021 01:47:07 GMT
EXPOSE 8888
# Sat, 10 Apr 2021 01:47:07 GMT
VOLUME [/var/lib/chronograf]
# Sat, 10 Apr 2021 01:47:07 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 10 Apr 2021 01:47:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 01:47:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b94e8b3cb7869f3c4a6438daab56a93381415beefa0cc91809c790d6fc396c9`  
		Last Modified: Sat, 10 Apr 2021 01:47:37 GMT  
		Size: 6.8 MB (6760279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770476205d15db72f48832a617c7fa91892ddccb7c3422be4ab97217a764eda8`  
		Last Modified: Sat, 10 Apr 2021 01:48:19 GMT  
		Size: 41.1 MB (41129581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125b6df1d4df29bef6ce3cee1d998fee3fad399c011f2a8afa4a0d5988d905f5`  
		Last Modified: Sat, 10 Apr 2021 01:48:13 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8e1406a19b23d67f40ca2d0066eb881d7c4e10b033dc6f9d8ba8a768a9a440`  
		Last Modified: Sat, 10 Apr 2021 01:48:13 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f93306a56a0605857f00b030fc4d3bded137a1c737c7c37716261e2c820cbe`  
		Last Modified: Sat, 10 Apr 2021 01:48:13 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f8aa43f5c6262d54ec3a88a9994814ee8e19c553bf47b4d64c0d520e32ce093e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63853612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c2c0f6a94429ec2396379b78b5defdbfe9fd92ce93cd455897b7c5a8ec82d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 30 Mar 2021 23:12:00 GMT
ADD file:acbde5217c39a55c2b477871bd72f5e796a00ff8fe549861a010b3585acf79c8 in / 
# Tue, 30 Mar 2021 23:12:03 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:14:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 31 Mar 2021 01:15:55 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Wed, 31 Mar 2021 01:16:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Mar 2021 01:16:20 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 31 Mar 2021 01:16:21 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 31 Mar 2021 01:16:22 GMT
EXPOSE 8888
# Wed, 31 Mar 2021 01:16:23 GMT
VOLUME [/var/lib/chronograf]
# Wed, 31 Mar 2021 01:16:24 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 31 Mar 2021 01:16:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 01:16:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6d58e1656f7868d0ecf4058d1f7d9d64560bbd4a5fff5a796f31171993a2da7c`  
		Last Modified: Tue, 30 Mar 2021 23:19:07 GMT  
		Size: 19.3 MB (19315190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede0b41a4840303eba6b7d45fc9aa8f389f9d8bad1151efeee8105b5f31f1b87`  
		Last Modified: Wed, 31 Mar 2021 01:16:51 GMT  
		Size: 5.8 MB (5779533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9514ec8c6a361715f3d7bb406fac5a8fe1c1b9a530780910ce458786fcb88d8`  
		Last Modified: Wed, 31 Mar 2021 01:17:33 GMT  
		Size: 38.7 MB (38734503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cf0bc57fd7f7bd7904255b04d9f05050164e57f2a03133a3fe53fadc5537f2`  
		Last Modified: Wed, 31 Mar 2021 01:17:23 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d328e23b7fe876fc5619166bf24fc6b870c14eaf2fb8d25b45d99602ad34cd17`  
		Last Modified: Wed, 31 Mar 2021 01:17:23 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f649a222fb0398e59bb1aeaa750dd8e69f27d20d1fb9766b1294a35cebfc11`  
		Last Modified: Wed, 31 Mar 2021 01:17:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:297b60973cd19e3cec05927c378b8c135bc913b235344c3b11aae1f2a8ed0d70
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f449b1271fccdbf7c501e4ce3a667a3842f21d3c1c748cb7c5a21a5686d0f497`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 10 Apr 2021 00:44:13 GMT
ADD file:a74d7856e70f2e18d2509edd9f0527254a69e9d1347715149c772a0d4ca7d509 in / 
# Sat, 10 Apr 2021 00:44:14 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 04:41:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 10 Apr 2021 04:42:32 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Sat, 10 Apr 2021 04:42:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 10 Apr 2021 04:42:47 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 10 Apr 2021 04:42:48 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 10 Apr 2021 04:42:49 GMT
EXPOSE 8888
# Sat, 10 Apr 2021 04:42:50 GMT
VOLUME [/var/lib/chronograf]
# Sat, 10 Apr 2021 04:42:51 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 10 Apr 2021 04:42:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 04:42:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:bc16ed4a30c7b74efb2ba46d7df8a6591a02826832c27a5cf55cc6e06111a5a6`  
		Last Modified: Sat, 10 Apr 2021 00:50:10 GMT  
		Size: 20.4 MB (20389366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c2ed72c66d02fd13b044d79fa58cf56d1a3ddb077cc81ccb643a341ab5eefb`  
		Last Modified: Sat, 10 Apr 2021 04:43:10 GMT  
		Size: 6.0 MB (6047617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24621004be61fb6cba386ce3e9263e0e426dff011731b0bb3118b4f0ad2c77ab`  
		Last Modified: Sat, 10 Apr 2021 04:43:52 GMT  
		Size: 38.5 MB (38502575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44434b3f85737bee2cce5ad3210338b916939a731119a5f6d66909e08196d01b`  
		Last Modified: Sat, 10 Apr 2021 04:43:40 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce8f3bdd5d029914779cae6b9dced855ae005ba2e884d7f86ecd3a633d1585d`  
		Last Modified: Sat, 10 Apr 2021 04:43:38 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c68e1532f0d9960688485eead7f17a36d5e44877ce90ac62c73dc217e2f68d`  
		Last Modified: Sat, 10 Apr 2021 04:43:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
