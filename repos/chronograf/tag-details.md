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
-	[`chronograf:1.8.10`](#chronograf1810)
-	[`chronograf:1.8.10-alpine`](#chronograf1810-alpine)
-	[`chronograf:1.9`](#chronograf19)
-	[`chronograf:1.9-alpine`](#chronograf19-alpine)
-	[`chronograf:1.9.4`](#chronograf194)
-	[`chronograf:1.9.4-alpine`](#chronograf194-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.6`

```console
$ docker pull chronograf@sha256:3f57ea8bfb0f32c0830922415237e0148a7a946e7be3577c7af1adc9d245393e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:52cc86bebef70178bd8a8e86fc213af12c1de605a28c1987efef82e866f47a02
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49397709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842b115490d38ea2c469ee25520891c34ccb8ac2d58a688bf485f961df925904`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 01:22:15 GMT
ADD file:026b786cdb9bd5132e483b55e6486a88dc97cd0f1dca7a128c56975e912865c3 in / 
# Wed, 11 May 2022 01:22:15 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:02:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 02:02:08 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 11 May 2022 02:02:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 02:02:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 02:02:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 02:02:16 GMT
EXPOSE 8888
# Wed, 11 May 2022 02:02:16 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 02:02:17 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 02:02:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 02:02:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d956d1d1888bd62aafc454609f2d7adc3a3ee5f9678bb80e4d9d27662c230884`  
		Last Modified: Wed, 11 May 2022 01:28:58 GMT  
		Size: 22.6 MB (22567372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b101a9563aaf479c6e6a826cb1d0b8dbd1e9dd761c31336ccf3a2713bddcc0af`  
		Last Modified: Wed, 11 May 2022 02:03:34 GMT  
		Size: 6.8 MB (6760320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e597f298bd5e6a4bdbc4b9cb8a5fcdaf48f7af68c5f1c273217ab639cc64ff6`  
		Last Modified: Wed, 11 May 2022 02:03:37 GMT  
		Size: 20.0 MB (20045625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382e07e653fcb4acc0fa52df2232df9e800069f9150fc8c30ec5fc507e28e3c3`  
		Last Modified: Wed, 11 May 2022 02:03:33 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad0677cdfb12a89f5c36fb2719fc0fe4d56361479b3d848a462786c1e4e7941`  
		Last Modified: Wed, 11 May 2022 02:03:33 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d32f603b2609c806b9c74e7703588cca6ab902cb1d57120b7215bb34e50bd9e`  
		Last Modified: Wed, 11 May 2022 02:03:33 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:396cea0cb25e6d7f3449c08dce063cf37a02f38b1375a3d5067ac72d3b486555
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43986022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485872c99c013d67f1ad8fec967b2ce1271d6452b728f883b01c22f8bbf93449`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 01:55:08 GMT
ADD file:2053868b10dc5164f3fb9b77a89aafd3da73e08ef244700b78666cc3e0f05b0f in / 
# Wed, 11 May 2022 01:55:09 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:59:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 03:59:41 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 11 May 2022 03:59:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 04:00:00 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 04:00:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 04:00:01 GMT
EXPOSE 8888
# Wed, 11 May 2022 04:00:01 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 04:00:02 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 04:00:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 04:00:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1b0318fd9d43e032add67ea408393c8e890c1ea4b437ecc600ea0107fa7de956`  
		Last Modified: Wed, 11 May 2022 02:11:56 GMT  
		Size: 19.4 MB (19359811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d6a8d215c465e56d8f308b31598d7cae73bef9a56e22a119d046b1440543d8`  
		Last Modified: Wed, 11 May 2022 04:03:24 GMT  
		Size: 5.8 MB (5780790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39840309a4c674deec53f32e15349dce12200bca8dd9d9f32384a8eb8566e5f`  
		Last Modified: Wed, 11 May 2022 04:03:34 GMT  
		Size: 18.8 MB (18821029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae593dc5dba110d1cdd0a1fd577bffece691aeb9c78dfc97f3fab04bd488eaa`  
		Last Modified: Wed, 11 May 2022 04:03:21 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca74c1f1e05a1b4e809aff1a4edf500d073916ea584e6edae746945765d5e0`  
		Last Modified: Wed, 11 May 2022 04:03:21 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f1724579d35f229b1f118eeecd51d95bde5c12463bbac0f840b2aa8856fdb4`  
		Last Modified: Wed, 11 May 2022 04:03:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b860453573152687086e7f4fcda8b143e34c1d8fa0fca4d122d45d95f59c863f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45456962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33747c892bb92910d47fb01e419d7067b2989fe8be3da2453bca1225b02d1af8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 00:49:23 GMT
ADD file:2da23cbf134c6ddbf47e6a21fd94f5d08453f8ea5b6d8c101c8a55408e61162c in / 
# Wed, 11 May 2022 00:49:24 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:41:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 01:41:15 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 11 May 2022 01:41:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 01:41:24 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 01:41:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 01:41:25 GMT
EXPOSE 8888
# Wed, 11 May 2022 01:41:26 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 01:41:28 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 01:41:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 01:41:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:716cebb420f77090ed0f738eb4ff36a4aff63f4b8bd8ad1e9fa099b3e2a53961`  
		Last Modified: Wed, 11 May 2022 00:57:53 GMT  
		Size: 20.4 MB (20423950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cab351856977abcb6226f57f9fd6c6b26d48a8040da752d217bed7142cf58d7`  
		Last Modified: Wed, 11 May 2022 01:43:09 GMT  
		Size: 6.0 MB (6047083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3fe843db732fb406c7ebf9df0109dc618a23b3d3a72a0eaa08282dd02e277d`  
		Last Modified: Wed, 11 May 2022 01:43:11 GMT  
		Size: 19.0 MB (18961535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f710f80e8de798ff295526b77e9087c9cdb67062c5d80e6f2ae0b5390f9b0d75`  
		Last Modified: Wed, 11 May 2022 01:43:08 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65d3c0bf7eeeb6f2e8e2effd6c5e57d12aeb59ea52facb551a82ae054267c58`  
		Last Modified: Wed, 11 May 2022 01:43:08 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e22670e808aa226c4c0cea2d3d8fe912e5675e2cd22a23d066a6a8911b9a145`  
		Last Modified: Wed, 11 May 2022 01:43:08 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6-alpine`

```console
$ docker pull chronograf@sha256:23417672f50b4d8e10c2afe16fb30256ea18d11c8b18476774bb7d582d31d80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6f8f433011148165c541c6c2b5a4e5b6a0e17ed7a30e489da79572ffb65511b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14852447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7955bca787a43198659959f56224c8b4bcdcec4f04756f3179ed0041b6b3c97a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:16 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 05 Apr 2022 04:26:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:20 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:20 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:20 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:20 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:21 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec6a02657fcad83f14ccaebfe65596c725dc1a85062cc10c59315a08a6b4139`  
		Last Modified: Tue, 05 Apr 2022 04:27:21 GMT  
		Size: 11.7 MB (11737836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f48b6b7852557acd0c24a3412aff3571ae06abe1235cec3ae3c10d78c63a7f`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 12.3 KB (12274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216f28bcf9418aa7355c3934973e69b52e1bba48dd0e758a66049eaef57cbd96`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d36456c8c8f7725ba610682fd161c3b25b5bc41b4a3e2a9d384a197f9d65cc0`  
		Last Modified: Tue, 05 Apr 2022 04:27:19 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2`

```console
$ docker pull chronograf@sha256:3f57ea8bfb0f32c0830922415237e0148a7a946e7be3577c7af1adc9d245393e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:52cc86bebef70178bd8a8e86fc213af12c1de605a28c1987efef82e866f47a02
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49397709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842b115490d38ea2c469ee25520891c34ccb8ac2d58a688bf485f961df925904`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 01:22:15 GMT
ADD file:026b786cdb9bd5132e483b55e6486a88dc97cd0f1dca7a128c56975e912865c3 in / 
# Wed, 11 May 2022 01:22:15 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:02:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 02:02:08 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 11 May 2022 02:02:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 02:02:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 02:02:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 02:02:16 GMT
EXPOSE 8888
# Wed, 11 May 2022 02:02:16 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 02:02:17 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 02:02:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 02:02:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d956d1d1888bd62aafc454609f2d7adc3a3ee5f9678bb80e4d9d27662c230884`  
		Last Modified: Wed, 11 May 2022 01:28:58 GMT  
		Size: 22.6 MB (22567372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b101a9563aaf479c6e6a826cb1d0b8dbd1e9dd761c31336ccf3a2713bddcc0af`  
		Last Modified: Wed, 11 May 2022 02:03:34 GMT  
		Size: 6.8 MB (6760320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e597f298bd5e6a4bdbc4b9cb8a5fcdaf48f7af68c5f1c273217ab639cc64ff6`  
		Last Modified: Wed, 11 May 2022 02:03:37 GMT  
		Size: 20.0 MB (20045625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382e07e653fcb4acc0fa52df2232df9e800069f9150fc8c30ec5fc507e28e3c3`  
		Last Modified: Wed, 11 May 2022 02:03:33 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad0677cdfb12a89f5c36fb2719fc0fe4d56361479b3d848a462786c1e4e7941`  
		Last Modified: Wed, 11 May 2022 02:03:33 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d32f603b2609c806b9c74e7703588cca6ab902cb1d57120b7215bb34e50bd9e`  
		Last Modified: Wed, 11 May 2022 02:03:33 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:396cea0cb25e6d7f3449c08dce063cf37a02f38b1375a3d5067ac72d3b486555
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43986022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485872c99c013d67f1ad8fec967b2ce1271d6452b728f883b01c22f8bbf93449`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 01:55:08 GMT
ADD file:2053868b10dc5164f3fb9b77a89aafd3da73e08ef244700b78666cc3e0f05b0f in / 
# Wed, 11 May 2022 01:55:09 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:59:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 03:59:41 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 11 May 2022 03:59:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 04:00:00 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 04:00:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 04:00:01 GMT
EXPOSE 8888
# Wed, 11 May 2022 04:00:01 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 04:00:02 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 04:00:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 04:00:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1b0318fd9d43e032add67ea408393c8e890c1ea4b437ecc600ea0107fa7de956`  
		Last Modified: Wed, 11 May 2022 02:11:56 GMT  
		Size: 19.4 MB (19359811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d6a8d215c465e56d8f308b31598d7cae73bef9a56e22a119d046b1440543d8`  
		Last Modified: Wed, 11 May 2022 04:03:24 GMT  
		Size: 5.8 MB (5780790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39840309a4c674deec53f32e15349dce12200bca8dd9d9f32384a8eb8566e5f`  
		Last Modified: Wed, 11 May 2022 04:03:34 GMT  
		Size: 18.8 MB (18821029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae593dc5dba110d1cdd0a1fd577bffece691aeb9c78dfc97f3fab04bd488eaa`  
		Last Modified: Wed, 11 May 2022 04:03:21 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca74c1f1e05a1b4e809aff1a4edf500d073916ea584e6edae746945765d5e0`  
		Last Modified: Wed, 11 May 2022 04:03:21 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f1724579d35f229b1f118eeecd51d95bde5c12463bbac0f840b2aa8856fdb4`  
		Last Modified: Wed, 11 May 2022 04:03:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b860453573152687086e7f4fcda8b143e34c1d8fa0fca4d122d45d95f59c863f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45456962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33747c892bb92910d47fb01e419d7067b2989fe8be3da2453bca1225b02d1af8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 00:49:23 GMT
ADD file:2da23cbf134c6ddbf47e6a21fd94f5d08453f8ea5b6d8c101c8a55408e61162c in / 
# Wed, 11 May 2022 00:49:24 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:41:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 01:41:15 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 11 May 2022 01:41:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 01:41:24 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 01:41:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 01:41:25 GMT
EXPOSE 8888
# Wed, 11 May 2022 01:41:26 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 01:41:28 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 01:41:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 01:41:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:716cebb420f77090ed0f738eb4ff36a4aff63f4b8bd8ad1e9fa099b3e2a53961`  
		Last Modified: Wed, 11 May 2022 00:57:53 GMT  
		Size: 20.4 MB (20423950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cab351856977abcb6226f57f9fd6c6b26d48a8040da752d217bed7142cf58d7`  
		Last Modified: Wed, 11 May 2022 01:43:09 GMT  
		Size: 6.0 MB (6047083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3fe843db732fb406c7ebf9df0109dc618a23b3d3a72a0eaa08282dd02e277d`  
		Last Modified: Wed, 11 May 2022 01:43:11 GMT  
		Size: 19.0 MB (18961535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f710f80e8de798ff295526b77e9087c9cdb67062c5d80e6f2ae0b5390f9b0d75`  
		Last Modified: Wed, 11 May 2022 01:43:08 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65d3c0bf7eeeb6f2e8e2effd6c5e57d12aeb59ea52facb551a82ae054267c58`  
		Last Modified: Wed, 11 May 2022 01:43:08 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e22670e808aa226c4c0cea2d3d8fe912e5675e2cd22a23d066a6a8911b9a145`  
		Last Modified: Wed, 11 May 2022 01:43:08 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2-alpine`

```console
$ docker pull chronograf@sha256:23417672f50b4d8e10c2afe16fb30256ea18d11c8b18476774bb7d582d31d80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6f8f433011148165c541c6c2b5a4e5b6a0e17ed7a30e489da79572ffb65511b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14852447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7955bca787a43198659959f56224c8b4bcdcec4f04756f3179ed0041b6b3c97a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:16 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 05 Apr 2022 04:26:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:20 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:20 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:20 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:20 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:21 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec6a02657fcad83f14ccaebfe65596c725dc1a85062cc10c59315a08a6b4139`  
		Last Modified: Tue, 05 Apr 2022 04:27:21 GMT  
		Size: 11.7 MB (11737836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f48b6b7852557acd0c24a3412aff3571ae06abe1235cec3ae3c10d78c63a7f`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 12.3 KB (12274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216f28bcf9418aa7355c3934973e69b52e1bba48dd0e758a66049eaef57cbd96`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d36456c8c8f7725ba610682fd161c3b25b5bc41b4a3e2a9d384a197f9d65cc0`  
		Last Modified: Tue, 05 Apr 2022 04:27:19 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:5fdf7fd8cea73d8cf50a3f13affc3221c91feed1ec3c8e4f6ef37acabd86039c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:76615861b03755bc372846d90d9cd516b798b78f141f21dfe48f474991301676
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65427084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4bf8aea22f5884538d25ed861a7916364306fee5caaf538fb2756ef8c8bebe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 01:22:15 GMT
ADD file:026b786cdb9bd5132e483b55e6486a88dc97cd0f1dca7a128c56975e912865c3 in / 
# Wed, 11 May 2022 01:22:15 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:02:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 02:02:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 11 May 2022 02:02:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 02:02:41 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 02:02:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 02:02:42 GMT
EXPOSE 8888
# Wed, 11 May 2022 02:02:42 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 02:02:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 02:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 02:02:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d956d1d1888bd62aafc454609f2d7adc3a3ee5f9678bb80e4d9d27662c230884`  
		Last Modified: Wed, 11 May 2022 01:28:58 GMT  
		Size: 22.6 MB (22567372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b4746a260bdba9e11b56e5ccbbdc3fe28ead34f46623e4fd8819764ec68902`  
		Last Modified: Wed, 11 May 2022 02:03:48 GMT  
		Size: 4.5 MB (4506810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0691b6670b22098b6992d17efb3c38473209a6aec8f11cf69f5a96ad30578f4`  
		Last Modified: Wed, 11 May 2022 02:03:52 GMT  
		Size: 38.3 MB (38328512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87c941bd1dcb93a128ce263db51e1ef2a41db201bbcdf4744aaae6dd30e3e25`  
		Last Modified: Wed, 11 May 2022 02:03:47 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6116e6ae6b620db3a3683fc78146e799dea29fcb7e1d41e084d4d9630b8f7e3b`  
		Last Modified: Wed, 11 May 2022 02:03:47 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e086796d811aaa2ee5bcc1f0018f1f12ed04128436ebb06141e3b48dff3eb0`  
		Last Modified: Wed, 11 May 2022 02:03:47 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:14235cd2bdc4af182e2d6dab6ee9f13a5e7cf7c7ded8411dd60a3016c0d244fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59048068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fceda010272732184cddb1c79ed3c41549dbb5158817e551ee0b33c85757ebf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 01:55:08 GMT
ADD file:2053868b10dc5164f3fb9b77a89aafd3da73e08ef244700b78666cc3e0f05b0f in / 
# Wed, 11 May 2022 01:55:09 GMT
CMD ["bash"]
# Wed, 11 May 2022 04:00:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 04:00:36 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 11 May 2022 04:01:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 04:01:10 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 04:01:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 04:01:11 GMT
EXPOSE 8888
# Wed, 11 May 2022 04:01:12 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 04:01:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 04:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 04:01:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1b0318fd9d43e032add67ea408393c8e890c1ea4b437ecc600ea0107fa7de956`  
		Last Modified: Wed, 11 May 2022 02:11:56 GMT  
		Size: 19.4 MB (19359811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a02543b217e9be575c73695108b8b5e62d80e8b97688caabdf2c5f0429225d`  
		Last Modified: Wed, 11 May 2022 04:03:47 GMT  
		Size: 3.9 MB (3880121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab3e920cb262b9d27b29fc7774f108d6a33a8e55e8755a1981c97a74e39cba7`  
		Last Modified: Wed, 11 May 2022 04:04:05 GMT  
		Size: 35.8 MB (35783737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f00f98b37435825aeebee78689092a57c5c8d36489396710a30fac7f3564517`  
		Last Modified: Wed, 11 May 2022 04:03:46 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d98299cef86b48fcb877e6b9e106b3ef30a765646ed688fa483e86abab5ca5d`  
		Last Modified: Wed, 11 May 2022 04:03:46 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436a035aac934c734801919ca8e1a84a9bc7c455dc58d552617751778cd3ec87`  
		Last Modified: Wed, 11 May 2022 04:03:46 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:45e6fb0cbe3605f170b05ecc36603cf0686b9d5bcdcc6cb43042d8a20d664cd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60329677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44a7a37d441809e60c5cb13caa7b22e50fbb6541f883f6cbe8fda64833ca8eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 00:49:23 GMT
ADD file:2da23cbf134c6ddbf47e6a21fd94f5d08453f8ea5b6d8c101c8a55408e61162c in / 
# Wed, 11 May 2022 00:49:24 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:41:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 01:41:43 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 11 May 2022 01:41:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 01:41:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 01:41:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 01:41:57 GMT
EXPOSE 8888
# Wed, 11 May 2022 01:41:58 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 01:42:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 01:42:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 01:42:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:716cebb420f77090ed0f738eb4ff36a4aff63f4b8bd8ad1e9fa099b3e2a53961`  
		Last Modified: Wed, 11 May 2022 00:57:53 GMT  
		Size: 20.4 MB (20423950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a466fa821308c649a5337c53b288d87f4129786553912d1c0f5fc376ab71e6c5`  
		Last Modified: Wed, 11 May 2022 01:43:22 GMT  
		Size: 3.9 MB (3893929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31568f094e45ded1d2842ff2fafcf330fa0b41be1c7f1ed824ff9e3e98544171`  
		Last Modified: Wed, 11 May 2022 01:43:26 GMT  
		Size: 36.0 MB (35987405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e589d71d96188798241b5a29cbe7ec51e182dc1cd38c52c01b34ff251d2fe277`  
		Last Modified: Wed, 11 May 2022 01:43:22 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251de6eb76634dbfc4cba0f69f734ee7b74d661cea71a2fc0485160d4db99486`  
		Last Modified: Wed, 11 May 2022 01:43:21 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da1ca9494ed5c1d21bd02b612cb4d6093c6bc698630a14ff2418622504253fe`  
		Last Modified: Wed, 11 May 2022 01:43:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:990421b8bc9b5dd6d472bd68efb5b165bf5f909c1b4a841756198933b14513d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:386f11aba61ccd79dd3d8105edce283d4eac402a7c92b802beb7ad89cf3136a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22670798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7c75f57862ead544bf92efebf86f59028a171990d14514c9cc621d7807042a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:26 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 05 Apr 2022 04:26:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:31 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:31 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:32 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:32 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8ba42ef9e34fc8eb0a6b88a3cd9242247e7029eaaed6b3d13f3f77eba9bb4f`  
		Last Modified: Tue, 05 Apr 2022 04:27:35 GMT  
		Size: 19.6 MB (19556196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e98e5f05434dd7e69e4acfb1c9682f93ab2c0d204b09dac76ccbc8fac82952`  
		Last Modified: Tue, 05 Apr 2022 04:27:32 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12636f40cb960e763e7c41f0b801007ade339c74aac79418124da7df48f27a7f`  
		Last Modified: Tue, 05 Apr 2022 04:27:32 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7c964b7b93ca840cc02a49bcee2e824dccd67e40f48c0d16b239cc3b3e2be1`  
		Last Modified: Tue, 05 Apr 2022 04:27:32 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:5fdf7fd8cea73d8cf50a3f13affc3221c91feed1ec3c8e4f6ef37acabd86039c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:76615861b03755bc372846d90d9cd516b798b78f141f21dfe48f474991301676
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65427084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4bf8aea22f5884538d25ed861a7916364306fee5caaf538fb2756ef8c8bebe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 01:22:15 GMT
ADD file:026b786cdb9bd5132e483b55e6486a88dc97cd0f1dca7a128c56975e912865c3 in / 
# Wed, 11 May 2022 01:22:15 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:02:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 02:02:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 11 May 2022 02:02:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 02:02:41 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 02:02:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 02:02:42 GMT
EXPOSE 8888
# Wed, 11 May 2022 02:02:42 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 02:02:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 02:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 02:02:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d956d1d1888bd62aafc454609f2d7adc3a3ee5f9678bb80e4d9d27662c230884`  
		Last Modified: Wed, 11 May 2022 01:28:58 GMT  
		Size: 22.6 MB (22567372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b4746a260bdba9e11b56e5ccbbdc3fe28ead34f46623e4fd8819764ec68902`  
		Last Modified: Wed, 11 May 2022 02:03:48 GMT  
		Size: 4.5 MB (4506810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0691b6670b22098b6992d17efb3c38473209a6aec8f11cf69f5a96ad30578f4`  
		Last Modified: Wed, 11 May 2022 02:03:52 GMT  
		Size: 38.3 MB (38328512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87c941bd1dcb93a128ce263db51e1ef2a41db201bbcdf4744aaae6dd30e3e25`  
		Last Modified: Wed, 11 May 2022 02:03:47 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6116e6ae6b620db3a3683fc78146e799dea29fcb7e1d41e084d4d9630b8f7e3b`  
		Last Modified: Wed, 11 May 2022 02:03:47 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e086796d811aaa2ee5bcc1f0018f1f12ed04128436ebb06141e3b48dff3eb0`  
		Last Modified: Wed, 11 May 2022 02:03:47 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:14235cd2bdc4af182e2d6dab6ee9f13a5e7cf7c7ded8411dd60a3016c0d244fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59048068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fceda010272732184cddb1c79ed3c41549dbb5158817e551ee0b33c85757ebf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 01:55:08 GMT
ADD file:2053868b10dc5164f3fb9b77a89aafd3da73e08ef244700b78666cc3e0f05b0f in / 
# Wed, 11 May 2022 01:55:09 GMT
CMD ["bash"]
# Wed, 11 May 2022 04:00:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 04:00:36 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 11 May 2022 04:01:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 04:01:10 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 04:01:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 04:01:11 GMT
EXPOSE 8888
# Wed, 11 May 2022 04:01:12 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 04:01:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 04:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 04:01:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1b0318fd9d43e032add67ea408393c8e890c1ea4b437ecc600ea0107fa7de956`  
		Last Modified: Wed, 11 May 2022 02:11:56 GMT  
		Size: 19.4 MB (19359811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a02543b217e9be575c73695108b8b5e62d80e8b97688caabdf2c5f0429225d`  
		Last Modified: Wed, 11 May 2022 04:03:47 GMT  
		Size: 3.9 MB (3880121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab3e920cb262b9d27b29fc7774f108d6a33a8e55e8755a1981c97a74e39cba7`  
		Last Modified: Wed, 11 May 2022 04:04:05 GMT  
		Size: 35.8 MB (35783737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f00f98b37435825aeebee78689092a57c5c8d36489396710a30fac7f3564517`  
		Last Modified: Wed, 11 May 2022 04:03:46 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d98299cef86b48fcb877e6b9e106b3ef30a765646ed688fa483e86abab5ca5d`  
		Last Modified: Wed, 11 May 2022 04:03:46 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436a035aac934c734801919ca8e1a84a9bc7c455dc58d552617751778cd3ec87`  
		Last Modified: Wed, 11 May 2022 04:03:46 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:45e6fb0cbe3605f170b05ecc36603cf0686b9d5bcdcc6cb43042d8a20d664cd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60329677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44a7a37d441809e60c5cb13caa7b22e50fbb6541f883f6cbe8fda64833ca8eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 00:49:23 GMT
ADD file:2da23cbf134c6ddbf47e6a21fd94f5d08453f8ea5b6d8c101c8a55408e61162c in / 
# Wed, 11 May 2022 00:49:24 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:41:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 01:41:43 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 11 May 2022 01:41:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 01:41:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 01:41:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 01:41:57 GMT
EXPOSE 8888
# Wed, 11 May 2022 01:41:58 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 01:42:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 01:42:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 01:42:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:716cebb420f77090ed0f738eb4ff36a4aff63f4b8bd8ad1e9fa099b3e2a53961`  
		Last Modified: Wed, 11 May 2022 00:57:53 GMT  
		Size: 20.4 MB (20423950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a466fa821308c649a5337c53b288d87f4129786553912d1c0f5fc376ab71e6c5`  
		Last Modified: Wed, 11 May 2022 01:43:22 GMT  
		Size: 3.9 MB (3893929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31568f094e45ded1d2842ff2fafcf330fa0b41be1c7f1ed824ff9e3e98544171`  
		Last Modified: Wed, 11 May 2022 01:43:26 GMT  
		Size: 36.0 MB (35987405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e589d71d96188798241b5a29cbe7ec51e182dc1cd38c52c01b34ff251d2fe277`  
		Last Modified: Wed, 11 May 2022 01:43:22 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251de6eb76634dbfc4cba0f69f734ee7b74d661cea71a2fc0485160d4db99486`  
		Last Modified: Wed, 11 May 2022 01:43:21 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da1ca9494ed5c1d21bd02b612cb4d6093c6bc698630a14ff2418622504253fe`  
		Last Modified: Wed, 11 May 2022 01:43:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:990421b8bc9b5dd6d472bd68efb5b165bf5f909c1b4a841756198933b14513d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:386f11aba61ccd79dd3d8105edce283d4eac402a7c92b802beb7ad89cf3136a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22670798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7c75f57862ead544bf92efebf86f59028a171990d14514c9cc621d7807042a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:26 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 05 Apr 2022 04:26:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:31 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:31 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:32 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:32 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8ba42ef9e34fc8eb0a6b88a3cd9242247e7029eaaed6b3d13f3f77eba9bb4f`  
		Last Modified: Tue, 05 Apr 2022 04:27:35 GMT  
		Size: 19.6 MB (19556196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e98e5f05434dd7e69e4acfb1c9682f93ab2c0d204b09dac76ccbc8fac82952`  
		Last Modified: Tue, 05 Apr 2022 04:27:32 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12636f40cb960e763e7c41f0b801007ade339c74aac79418124da7df48f27a7f`  
		Last Modified: Tue, 05 Apr 2022 04:27:32 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7c964b7b93ca840cc02a49bcee2e824dccd67e40f48c0d16b239cc3b3e2be1`  
		Last Modified: Tue, 05 Apr 2022 04:27:32 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:63b6425ea2a393146632303095637cd2c03a550e2f67f01eed12d6503f78386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:35b9e6ee6ac3508b9a153601aee0782efd032c3209d9cb2eeda742cea1790e29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66278714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688e7e5fb4831aff3eb177714ce2fdf552ab614a85d2bcd72734a0a87d36483e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 01:22:15 GMT
ADD file:026b786cdb9bd5132e483b55e6486a88dc97cd0f1dca7a128c56975e912865c3 in / 
# Wed, 11 May 2022 01:22:15 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:02:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 02:02:48 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 11 May 2022 02:02:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 02:02:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 02:02:56 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 02:02:56 GMT
EXPOSE 8888
# Wed, 11 May 2022 02:02:57 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 02:02:57 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 02:02:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 02:02:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d956d1d1888bd62aafc454609f2d7adc3a3ee5f9678bb80e4d9d27662c230884`  
		Last Modified: Wed, 11 May 2022 01:28:58 GMT  
		Size: 22.6 MB (22567372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b101a9563aaf479c6e6a826cb1d0b8dbd1e9dd761c31336ccf3a2713bddcc0af`  
		Last Modified: Wed, 11 May 2022 02:03:34 GMT  
		Size: 6.8 MB (6760320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5abff4dab5db07351fb6ca9cbffb01a983690bbd985db40d18b3c5b1cf1169`  
		Last Modified: Wed, 11 May 2022 02:04:07 GMT  
		Size: 36.9 MB (36926639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc83279cfcd78e61edc718db0f82434669882ef8a5a32b053ded52296d6672ef`  
		Last Modified: Wed, 11 May 2022 02:04:03 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f583b5b90b3b15349aaefbd3a990ec7f99453ede4b9d61896d6ac04ba0ae39f`  
		Last Modified: Wed, 11 May 2022 02:04:02 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff009efa48f0ca6e29791dda4c4d71df8161260357921a70f57f8fcfe7e3bf32`  
		Last Modified: Wed, 11 May 2022 02:04:02 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ab0a07c967d5ab06e1d74056c0e8316e7b7c8459746f44e389a8dbf27e827762
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59677004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6e101d3a49cdc02538c9e7010d5c5668281729500bacd71a6ba4ee283d1e58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 01:55:08 GMT
ADD file:2053868b10dc5164f3fb9b77a89aafd3da73e08ef244700b78666cc3e0f05b0f in / 
# Wed, 11 May 2022 01:55:09 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:59:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 04:01:29 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 11 May 2022 04:01:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 04:01:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 04:01:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 04:01:51 GMT
EXPOSE 8888
# Wed, 11 May 2022 04:01:51 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 04:01:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 04:01:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 04:01:53 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1b0318fd9d43e032add67ea408393c8e890c1ea4b437ecc600ea0107fa7de956`  
		Last Modified: Wed, 11 May 2022 02:11:56 GMT  
		Size: 19.4 MB (19359811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d6a8d215c465e56d8f308b31598d7cae73bef9a56e22a119d046b1440543d8`  
		Last Modified: Wed, 11 May 2022 04:03:24 GMT  
		Size: 5.8 MB (5780790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c975fa626f90c55236aa195b47069e63a3bacf49263a5da986ddec5ee621232`  
		Last Modified: Wed, 11 May 2022 04:04:35 GMT  
		Size: 34.5 MB (34512010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e8c34a7ea01f20037ff9795a8899bf9e79008c717ac878d0fae5a610bd350a`  
		Last Modified: Wed, 11 May 2022 04:04:17 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa17c3bd86eaf0cdea07e1f50b1fd814b2691cd7eff76002a0b1fee55133613`  
		Last Modified: Wed, 11 May 2022 04:04:17 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9419c7e9729cc43647b703d6700f719d369f59bfa48eee5ce0a35dc59ec600ba`  
		Last Modified: Wed, 11 May 2022 04:04:17 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c6ed530c28b16dd07fda172bf5234774598228a51d57bef0dfae09a029d4d40e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60927011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f57dca1cfe468ab95fab79d442fde62b33ee1d323a507c4c2a068201052b156`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 00:49:23 GMT
ADD file:2da23cbf134c6ddbf47e6a21fd94f5d08453f8ea5b6d8c101c8a55408e61162c in / 
# Wed, 11 May 2022 00:49:24 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:41:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 01:42:06 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 11 May 2022 01:42:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 01:42:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 01:42:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 01:42:17 GMT
EXPOSE 8888
# Wed, 11 May 2022 01:42:18 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 01:42:20 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 01:42:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 01:42:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:716cebb420f77090ed0f738eb4ff36a4aff63f4b8bd8ad1e9fa099b3e2a53961`  
		Last Modified: Wed, 11 May 2022 00:57:53 GMT  
		Size: 20.4 MB (20423950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cab351856977abcb6226f57f9fd6c6b26d48a8040da752d217bed7142cf58d7`  
		Last Modified: Wed, 11 May 2022 01:43:09 GMT  
		Size: 6.0 MB (6047083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ac0d88180e26973389cae868f04ca6f147730ec0104c8160ba1b23f1bf116f`  
		Last Modified: Wed, 11 May 2022 01:43:42 GMT  
		Size: 34.4 MB (34431587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d24cff9cd03ba94d927f89546958e43438d052b0c4654b53fd2f354c1d0adc9`  
		Last Modified: Wed, 11 May 2022 01:43:37 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c8d8da3d9fc43287b9151ee8dcc33d798581563039c55a8a9cdf03f181dc93`  
		Last Modified: Wed, 11 May 2022 01:43:37 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a1d57b7f59a59ae8ed42a81cf26cf2eca65e382106ac84ec65ed76f1e134a5`  
		Last Modified: Wed, 11 May 2022 01:43:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:d3e3bbce6ab55cead013b905eba19cdd95cc418e5f2acfb421159ccc1bf8cbd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b28beb85949241c005e5be21181999ce565e4b29dd96295f7e2f7d8ff833a80a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22318581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb7b4f19d3448b5e558e8d6e7857db12751a4b8a0928e3f0fa36efaa296650b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:37 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 05 Apr 2022 04:26:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:43 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:43 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:43 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e780df476439b3a8749d6d1ec5009124d7cb47b7328d520390e5c1df5e5260f7`  
		Last Modified: Tue, 05 Apr 2022 04:27:49 GMT  
		Size: 19.2 MB (19203976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770779eb24c794631aa560ebb5145f2fd7a4bf2972a43459d9321581fc47084e`  
		Last Modified: Tue, 05 Apr 2022 04:27:45 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e1701788eafedc43dca0570322f1ab0c00388a8d9a882173a472e4cc23774b`  
		Last Modified: Tue, 05 Apr 2022 04:27:45 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51eec10863e13223024d57ee99337a425873b97b7b2829d8f207c267a414b201`  
		Last Modified: Tue, 05 Apr 2022 04:27:45 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:63b6425ea2a393146632303095637cd2c03a550e2f67f01eed12d6503f78386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:35b9e6ee6ac3508b9a153601aee0782efd032c3209d9cb2eeda742cea1790e29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66278714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688e7e5fb4831aff3eb177714ce2fdf552ab614a85d2bcd72734a0a87d36483e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 01:22:15 GMT
ADD file:026b786cdb9bd5132e483b55e6486a88dc97cd0f1dca7a128c56975e912865c3 in / 
# Wed, 11 May 2022 01:22:15 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:02:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 02:02:48 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 11 May 2022 02:02:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 02:02:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 02:02:56 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 02:02:56 GMT
EXPOSE 8888
# Wed, 11 May 2022 02:02:57 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 02:02:57 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 02:02:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 02:02:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d956d1d1888bd62aafc454609f2d7adc3a3ee5f9678bb80e4d9d27662c230884`  
		Last Modified: Wed, 11 May 2022 01:28:58 GMT  
		Size: 22.6 MB (22567372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b101a9563aaf479c6e6a826cb1d0b8dbd1e9dd761c31336ccf3a2713bddcc0af`  
		Last Modified: Wed, 11 May 2022 02:03:34 GMT  
		Size: 6.8 MB (6760320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5abff4dab5db07351fb6ca9cbffb01a983690bbd985db40d18b3c5b1cf1169`  
		Last Modified: Wed, 11 May 2022 02:04:07 GMT  
		Size: 36.9 MB (36926639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc83279cfcd78e61edc718db0f82434669882ef8a5a32b053ded52296d6672ef`  
		Last Modified: Wed, 11 May 2022 02:04:03 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f583b5b90b3b15349aaefbd3a990ec7f99453ede4b9d61896d6ac04ba0ae39f`  
		Last Modified: Wed, 11 May 2022 02:04:02 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff009efa48f0ca6e29791dda4c4d71df8161260357921a70f57f8fcfe7e3bf32`  
		Last Modified: Wed, 11 May 2022 02:04:02 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ab0a07c967d5ab06e1d74056c0e8316e7b7c8459746f44e389a8dbf27e827762
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59677004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6e101d3a49cdc02538c9e7010d5c5668281729500bacd71a6ba4ee283d1e58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 01:55:08 GMT
ADD file:2053868b10dc5164f3fb9b77a89aafd3da73e08ef244700b78666cc3e0f05b0f in / 
# Wed, 11 May 2022 01:55:09 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:59:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 04:01:29 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 11 May 2022 04:01:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 04:01:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 04:01:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 04:01:51 GMT
EXPOSE 8888
# Wed, 11 May 2022 04:01:51 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 04:01:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 04:01:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 04:01:53 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1b0318fd9d43e032add67ea408393c8e890c1ea4b437ecc600ea0107fa7de956`  
		Last Modified: Wed, 11 May 2022 02:11:56 GMT  
		Size: 19.4 MB (19359811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d6a8d215c465e56d8f308b31598d7cae73bef9a56e22a119d046b1440543d8`  
		Last Modified: Wed, 11 May 2022 04:03:24 GMT  
		Size: 5.8 MB (5780790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c975fa626f90c55236aa195b47069e63a3bacf49263a5da986ddec5ee621232`  
		Last Modified: Wed, 11 May 2022 04:04:35 GMT  
		Size: 34.5 MB (34512010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e8c34a7ea01f20037ff9795a8899bf9e79008c717ac878d0fae5a610bd350a`  
		Last Modified: Wed, 11 May 2022 04:04:17 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa17c3bd86eaf0cdea07e1f50b1fd814b2691cd7eff76002a0b1fee55133613`  
		Last Modified: Wed, 11 May 2022 04:04:17 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9419c7e9729cc43647b703d6700f719d369f59bfa48eee5ce0a35dc59ec600ba`  
		Last Modified: Wed, 11 May 2022 04:04:17 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c6ed530c28b16dd07fda172bf5234774598228a51d57bef0dfae09a029d4d40e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60927011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f57dca1cfe468ab95fab79d442fde62b33ee1d323a507c4c2a068201052b156`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 00:49:23 GMT
ADD file:2da23cbf134c6ddbf47e6a21fd94f5d08453f8ea5b6d8c101c8a55408e61162c in / 
# Wed, 11 May 2022 00:49:24 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:41:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 01:42:06 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 11 May 2022 01:42:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 01:42:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 01:42:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 01:42:17 GMT
EXPOSE 8888
# Wed, 11 May 2022 01:42:18 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 01:42:20 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 01:42:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 01:42:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:716cebb420f77090ed0f738eb4ff36a4aff63f4b8bd8ad1e9fa099b3e2a53961`  
		Last Modified: Wed, 11 May 2022 00:57:53 GMT  
		Size: 20.4 MB (20423950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cab351856977abcb6226f57f9fd6c6b26d48a8040da752d217bed7142cf58d7`  
		Last Modified: Wed, 11 May 2022 01:43:09 GMT  
		Size: 6.0 MB (6047083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ac0d88180e26973389cae868f04ca6f147730ec0104c8160ba1b23f1bf116f`  
		Last Modified: Wed, 11 May 2022 01:43:42 GMT  
		Size: 34.4 MB (34431587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d24cff9cd03ba94d927f89546958e43438d052b0c4654b53fd2f354c1d0adc9`  
		Last Modified: Wed, 11 May 2022 01:43:37 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c8d8da3d9fc43287b9151ee8dcc33d798581563039c55a8a9cdf03f181dc93`  
		Last Modified: Wed, 11 May 2022 01:43:37 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a1d57b7f59a59ae8ed42a81cf26cf2eca65e382106ac84ec65ed76f1e134a5`  
		Last Modified: Wed, 11 May 2022 01:43:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:d3e3bbce6ab55cead013b905eba19cdd95cc418e5f2acfb421159ccc1bf8cbd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b28beb85949241c005e5be21181999ce565e4b29dd96295f7e2f7d8ff833a80a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22318581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb7b4f19d3448b5e558e8d6e7857db12751a4b8a0928e3f0fa36efaa296650b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:37 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 05 Apr 2022 04:26:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:43 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:43 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:43 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e780df476439b3a8749d6d1ec5009124d7cb47b7328d520390e5c1df5e5260f7`  
		Last Modified: Tue, 05 Apr 2022 04:27:49 GMT  
		Size: 19.2 MB (19203976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770779eb24c794631aa560ebb5145f2fd7a4bf2972a43459d9321581fc47084e`  
		Last Modified: Tue, 05 Apr 2022 04:27:45 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e1701788eafedc43dca0570322f1ab0c00388a8d9a882173a472e4cc23774b`  
		Last Modified: Tue, 05 Apr 2022 04:27:45 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51eec10863e13223024d57ee99337a425873b97b7b2829d8f207c267a414b201`  
		Last Modified: Tue, 05 Apr 2022 04:27:45 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:618af93b3d2c1aa4d4291f1d5f86012f73fc1d6b4819a02c3e8c909c6c871473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:05acb1424d9df481ef30b91162e471c1bf2a2b9ffc3781379fa3014eb2d188c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66922495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8a56592ea3187da90ad58713b5a5417794f061d3faf6c0300b889e1990a1bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 01:22:15 GMT
ADD file:026b786cdb9bd5132e483b55e6486a88dc97cd0f1dca7a128c56975e912865c3 in / 
# Wed, 11 May 2022 01:22:15 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:02:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 02:03:01 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 11 May 2022 02:03:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 02:03:10 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 02:03:10 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 02:03:10 GMT
EXPOSE 8888
# Wed, 11 May 2022 02:03:10 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 02:03:10 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 02:03:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 02:03:10 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d956d1d1888bd62aafc454609f2d7adc3a3ee5f9678bb80e4d9d27662c230884`  
		Last Modified: Wed, 11 May 2022 01:28:58 GMT  
		Size: 22.6 MB (22567372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b101a9563aaf479c6e6a826cb1d0b8dbd1e9dd761c31336ccf3a2713bddcc0af`  
		Last Modified: Wed, 11 May 2022 02:03:34 GMT  
		Size: 6.8 MB (6760320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb73533d257fdcc9847436a60319f4b50f8c06542f163436e8054366594514c`  
		Last Modified: Wed, 11 May 2022 02:04:23 GMT  
		Size: 37.6 MB (37570407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c18f47335a5f18457b213872f97a94bbdba37b55340b52fcd39d57ff8a3f2a`  
		Last Modified: Wed, 11 May 2022 02:04:18 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb738848ef88f9be27f61bac046e07d679c0cac03c494400013c9250d6c87c7`  
		Last Modified: Wed, 11 May 2022 02:04:18 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4978a3ccc48c72a9c6d1e815af4bde43ce71d46333ed4508834dd6595356b78`  
		Last Modified: Wed, 11 May 2022 02:04:18 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:bde5d1d3b73f3bad65bee41d9113d461cb7fdc0bebfdd84a750b21d5583abd3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60456521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf7614eb0a491e36eabb91aefd5a152d59a46914688bd71fd8406b2b739ad68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 01:55:08 GMT
ADD file:2053868b10dc5164f3fb9b77a89aafd3da73e08ef244700b78666cc3e0f05b0f in / 
# Wed, 11 May 2022 01:55:09 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:59:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 04:02:05 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 11 May 2022 04:02:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 04:02:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 04:02:26 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 04:02:26 GMT
EXPOSE 8888
# Wed, 11 May 2022 04:02:27 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 04:02:27 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 04:02:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 04:02:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1b0318fd9d43e032add67ea408393c8e890c1ea4b437ecc600ea0107fa7de956`  
		Last Modified: Wed, 11 May 2022 02:11:56 GMT  
		Size: 19.4 MB (19359811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d6a8d215c465e56d8f308b31598d7cae73bef9a56e22a119d046b1440543d8`  
		Last Modified: Wed, 11 May 2022 04:03:24 GMT  
		Size: 5.8 MB (5780790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5a52e918af5f03a1416f801974f3730a5206537f17f46378fa67429c24e0ae`  
		Last Modified: Wed, 11 May 2022 04:05:05 GMT  
		Size: 35.3 MB (35291525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec39b317801752ad6eb2655215fa70797d5c161dd16caac8a031fa88926eb3c`  
		Last Modified: Wed, 11 May 2022 04:04:46 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c2a374c530fb20edb0d1039fa77753ae7f93f6921f8daabea00d8cb215d8c3`  
		Last Modified: Wed, 11 May 2022 04:04:46 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3911fdd86e9472e6f9bf5e0628aae4e9031d6fe8be9f792bd77383dd6ece0a`  
		Last Modified: Wed, 11 May 2022 04:04:46 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:14f815ef09eadcb495bc7686cd97aff68c0c327688f6a7bd91c967d04e7751dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61669454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8be3b5f87826c735222de2bcbfc1df70472048ba777023c05823b9bf5d856ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 00:49:23 GMT
ADD file:2da23cbf134c6ddbf47e6a21fd94f5d08453f8ea5b6d8c101c8a55408e61162c in / 
# Wed, 11 May 2022 00:49:24 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:41:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 01:42:26 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 11 May 2022 01:42:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 01:42:36 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 01:42:37 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 01:42:37 GMT
EXPOSE 8888
# Wed, 11 May 2022 01:42:38 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 01:42:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 01:42:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 01:42:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:716cebb420f77090ed0f738eb4ff36a4aff63f4b8bd8ad1e9fa099b3e2a53961`  
		Last Modified: Wed, 11 May 2022 00:57:53 GMT  
		Size: 20.4 MB (20423950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cab351856977abcb6226f57f9fd6c6b26d48a8040da752d217bed7142cf58d7`  
		Last Modified: Wed, 11 May 2022 01:43:09 GMT  
		Size: 6.0 MB (6047083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad109811dad6305323b0c0483ec91a900e6119f794fa884188f958d56b22a5b`  
		Last Modified: Wed, 11 May 2022 01:43:57 GMT  
		Size: 35.2 MB (35174032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38515e26a218f5e1a76f36cdcbdb63cb6edf55c36da28becf537f0e3408dfdbe`  
		Last Modified: Wed, 11 May 2022 01:43:53 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07949b7bfb3ceabbf18d5db8f0640413eb00e8cb2c538b9ab9c942f1694e66d`  
		Last Modified: Wed, 11 May 2022 01:43:52 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acfe2694f6dc110bee371500c48c3ab959fb6e008449228f920548a56bbdefc`  
		Last Modified: Wed, 11 May 2022 01:43:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:64529a79e1f42f21063f77e88d3b17a66dd5fe12b361ba459a496564f60deae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:617112048d88886c7c56a0298d5022925bf60cea583bf42950f85da0b1543c30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22786740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f641fefba39a03a8fb9f9a028aeeecec9f62c81b6a89da22334192b42afee733`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:47 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 05 Apr 2022 04:26:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:55 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:55 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:56 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03048cd652ea5c71fdf0fb436e4b84f533bce10501e6f8f75b34a3f5499ec3bc`  
		Last Modified: Tue, 05 Apr 2022 04:28:03 GMT  
		Size: 19.7 MB (19672143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcafdf6394d7dc10583226357da386688d2d1aa89d90e9d6c3e02d059d1ff7a0`  
		Last Modified: Tue, 05 Apr 2022 04:27:59 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9df35e5b1a70215f7fa195a06d17ece074a61ec14d91da8c065c6f5426b8bc`  
		Last Modified: Tue, 05 Apr 2022 04:27:59 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eab2c8d98b5fdc4d6ed0e531c9766afacad54ccd952085aa98da4d57c5519a`  
		Last Modified: Tue, 05 Apr 2022 04:28:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:618af93b3d2c1aa4d4291f1d5f86012f73fc1d6b4819a02c3e8c909c6c871473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:05acb1424d9df481ef30b91162e471c1bf2a2b9ffc3781379fa3014eb2d188c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66922495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8a56592ea3187da90ad58713b5a5417794f061d3faf6c0300b889e1990a1bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 01:22:15 GMT
ADD file:026b786cdb9bd5132e483b55e6486a88dc97cd0f1dca7a128c56975e912865c3 in / 
# Wed, 11 May 2022 01:22:15 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:02:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 02:03:01 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 11 May 2022 02:03:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 02:03:10 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 02:03:10 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 02:03:10 GMT
EXPOSE 8888
# Wed, 11 May 2022 02:03:10 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 02:03:10 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 02:03:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 02:03:10 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d956d1d1888bd62aafc454609f2d7adc3a3ee5f9678bb80e4d9d27662c230884`  
		Last Modified: Wed, 11 May 2022 01:28:58 GMT  
		Size: 22.6 MB (22567372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b101a9563aaf479c6e6a826cb1d0b8dbd1e9dd761c31336ccf3a2713bddcc0af`  
		Last Modified: Wed, 11 May 2022 02:03:34 GMT  
		Size: 6.8 MB (6760320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb73533d257fdcc9847436a60319f4b50f8c06542f163436e8054366594514c`  
		Last Modified: Wed, 11 May 2022 02:04:23 GMT  
		Size: 37.6 MB (37570407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c18f47335a5f18457b213872f97a94bbdba37b55340b52fcd39d57ff8a3f2a`  
		Last Modified: Wed, 11 May 2022 02:04:18 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb738848ef88f9be27f61bac046e07d679c0cac03c494400013c9250d6c87c7`  
		Last Modified: Wed, 11 May 2022 02:04:18 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4978a3ccc48c72a9c6d1e815af4bde43ce71d46333ed4508834dd6595356b78`  
		Last Modified: Wed, 11 May 2022 02:04:18 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:bde5d1d3b73f3bad65bee41d9113d461cb7fdc0bebfdd84a750b21d5583abd3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60456521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf7614eb0a491e36eabb91aefd5a152d59a46914688bd71fd8406b2b739ad68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 01:55:08 GMT
ADD file:2053868b10dc5164f3fb9b77a89aafd3da73e08ef244700b78666cc3e0f05b0f in / 
# Wed, 11 May 2022 01:55:09 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:59:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 04:02:05 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 11 May 2022 04:02:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 04:02:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 04:02:26 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 04:02:26 GMT
EXPOSE 8888
# Wed, 11 May 2022 04:02:27 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 04:02:27 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 04:02:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 04:02:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1b0318fd9d43e032add67ea408393c8e890c1ea4b437ecc600ea0107fa7de956`  
		Last Modified: Wed, 11 May 2022 02:11:56 GMT  
		Size: 19.4 MB (19359811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d6a8d215c465e56d8f308b31598d7cae73bef9a56e22a119d046b1440543d8`  
		Last Modified: Wed, 11 May 2022 04:03:24 GMT  
		Size: 5.8 MB (5780790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5a52e918af5f03a1416f801974f3730a5206537f17f46378fa67429c24e0ae`  
		Last Modified: Wed, 11 May 2022 04:05:05 GMT  
		Size: 35.3 MB (35291525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec39b317801752ad6eb2655215fa70797d5c161dd16caac8a031fa88926eb3c`  
		Last Modified: Wed, 11 May 2022 04:04:46 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c2a374c530fb20edb0d1039fa77753ae7f93f6921f8daabea00d8cb215d8c3`  
		Last Modified: Wed, 11 May 2022 04:04:46 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3911fdd86e9472e6f9bf5e0628aae4e9031d6fe8be9f792bd77383dd6ece0a`  
		Last Modified: Wed, 11 May 2022 04:04:46 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:14f815ef09eadcb495bc7686cd97aff68c0c327688f6a7bd91c967d04e7751dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61669454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8be3b5f87826c735222de2bcbfc1df70472048ba777023c05823b9bf5d856ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 00:49:23 GMT
ADD file:2da23cbf134c6ddbf47e6a21fd94f5d08453f8ea5b6d8c101c8a55408e61162c in / 
# Wed, 11 May 2022 00:49:24 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:41:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 01:42:26 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 11 May 2022 01:42:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 01:42:36 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 01:42:37 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 01:42:37 GMT
EXPOSE 8888
# Wed, 11 May 2022 01:42:38 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 01:42:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 01:42:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 01:42:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:716cebb420f77090ed0f738eb4ff36a4aff63f4b8bd8ad1e9fa099b3e2a53961`  
		Last Modified: Wed, 11 May 2022 00:57:53 GMT  
		Size: 20.4 MB (20423950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cab351856977abcb6226f57f9fd6c6b26d48a8040da752d217bed7142cf58d7`  
		Last Modified: Wed, 11 May 2022 01:43:09 GMT  
		Size: 6.0 MB (6047083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad109811dad6305323b0c0483ec91a900e6119f794fa884188f958d56b22a5b`  
		Last Modified: Wed, 11 May 2022 01:43:57 GMT  
		Size: 35.2 MB (35174032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38515e26a218f5e1a76f36cdcbdb63cb6edf55c36da28becf537f0e3408dfdbe`  
		Last Modified: Wed, 11 May 2022 01:43:53 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07949b7bfb3ceabbf18d5db8f0640413eb00e8cb2c538b9ab9c942f1694e66d`  
		Last Modified: Wed, 11 May 2022 01:43:52 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acfe2694f6dc110bee371500c48c3ab959fb6e008449228f920548a56bbdefc`  
		Last Modified: Wed, 11 May 2022 01:43:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:64529a79e1f42f21063f77e88d3b17a66dd5fe12b361ba459a496564f60deae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:617112048d88886c7c56a0298d5022925bf60cea583bf42950f85da0b1543c30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22786740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f641fefba39a03a8fb9f9a028aeeecec9f62c81b6a89da22334192b42afee733`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:47 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 05 Apr 2022 04:26:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:55 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:55 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:56 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03048cd652ea5c71fdf0fb436e4b84f533bce10501e6f8f75b34a3f5499ec3bc`  
		Last Modified: Tue, 05 Apr 2022 04:28:03 GMT  
		Size: 19.7 MB (19672143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcafdf6394d7dc10583226357da386688d2d1aa89d90e9d6c3e02d059d1ff7a0`  
		Last Modified: Tue, 05 Apr 2022 04:27:59 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9df35e5b1a70215f7fa195a06d17ece074a61ec14d91da8c065c6f5426b8bc`  
		Last Modified: Tue, 05 Apr 2022 04:27:59 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eab2c8d98b5fdc4d6ed0e531c9766afacad54ccd952085aa98da4d57c5519a`  
		Last Modified: Tue, 05 Apr 2022 04:28:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:64529a79e1f42f21063f77e88d3b17a66dd5fe12b361ba459a496564f60deae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:617112048d88886c7c56a0298d5022925bf60cea583bf42950f85da0b1543c30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22786740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f641fefba39a03a8fb9f9a028aeeecec9f62c81b6a89da22334192b42afee733`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:26:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:26:16 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 05 Apr 2022 04:26:47 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 05 Apr 2022 04:26:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 05 Apr 2022 04:26:55 GMT
EXPOSE 8888
# Tue, 05 Apr 2022 04:26:55 GMT
VOLUME [/var/lib/chronograf]
# Tue, 05 Apr 2022 04:26:55 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 05 Apr 2022 04:26:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 04:26:56 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cc030286fba3c1f3131d94752cdc227e840c98131bf4fa7ae057a8e624e0cc`  
		Last Modified: Tue, 05 Apr 2022 04:27:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beb826c7b7288de69f85c4476fd6f04b58ceed760dd1b9e51a7d80aeb0e471`  
		Last Modified: Tue, 05 Apr 2022 04:27:20 GMT  
		Size: 271.7 KB (271678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03048cd652ea5c71fdf0fb436e4b84f533bce10501e6f8f75b34a3f5499ec3bc`  
		Last Modified: Tue, 05 Apr 2022 04:28:03 GMT  
		Size: 19.7 MB (19672143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcafdf6394d7dc10583226357da386688d2d1aa89d90e9d6c3e02d059d1ff7a0`  
		Last Modified: Tue, 05 Apr 2022 04:27:59 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9df35e5b1a70215f7fa195a06d17ece074a61ec14d91da8c065c6f5426b8bc`  
		Last Modified: Tue, 05 Apr 2022 04:27:59 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eab2c8d98b5fdc4d6ed0e531c9766afacad54ccd952085aa98da4d57c5519a`  
		Last Modified: Tue, 05 Apr 2022 04:28:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:618af93b3d2c1aa4d4291f1d5f86012f73fc1d6b4819a02c3e8c909c6c871473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:05acb1424d9df481ef30b91162e471c1bf2a2b9ffc3781379fa3014eb2d188c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66922495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8a56592ea3187da90ad58713b5a5417794f061d3faf6c0300b889e1990a1bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 01:22:15 GMT
ADD file:026b786cdb9bd5132e483b55e6486a88dc97cd0f1dca7a128c56975e912865c3 in / 
# Wed, 11 May 2022 01:22:15 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:02:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 02:03:01 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 11 May 2022 02:03:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 02:03:10 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 02:03:10 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 02:03:10 GMT
EXPOSE 8888
# Wed, 11 May 2022 02:03:10 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 02:03:10 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 02:03:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 02:03:10 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d956d1d1888bd62aafc454609f2d7adc3a3ee5f9678bb80e4d9d27662c230884`  
		Last Modified: Wed, 11 May 2022 01:28:58 GMT  
		Size: 22.6 MB (22567372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b101a9563aaf479c6e6a826cb1d0b8dbd1e9dd761c31336ccf3a2713bddcc0af`  
		Last Modified: Wed, 11 May 2022 02:03:34 GMT  
		Size: 6.8 MB (6760320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb73533d257fdcc9847436a60319f4b50f8c06542f163436e8054366594514c`  
		Last Modified: Wed, 11 May 2022 02:04:23 GMT  
		Size: 37.6 MB (37570407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c18f47335a5f18457b213872f97a94bbdba37b55340b52fcd39d57ff8a3f2a`  
		Last Modified: Wed, 11 May 2022 02:04:18 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb738848ef88f9be27f61bac046e07d679c0cac03c494400013c9250d6c87c7`  
		Last Modified: Wed, 11 May 2022 02:04:18 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4978a3ccc48c72a9c6d1e815af4bde43ce71d46333ed4508834dd6595356b78`  
		Last Modified: Wed, 11 May 2022 02:04:18 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:bde5d1d3b73f3bad65bee41d9113d461cb7fdc0bebfdd84a750b21d5583abd3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60456521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf7614eb0a491e36eabb91aefd5a152d59a46914688bd71fd8406b2b739ad68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 01:55:08 GMT
ADD file:2053868b10dc5164f3fb9b77a89aafd3da73e08ef244700b78666cc3e0f05b0f in / 
# Wed, 11 May 2022 01:55:09 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:59:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 04:02:05 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 11 May 2022 04:02:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 04:02:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 04:02:26 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 04:02:26 GMT
EXPOSE 8888
# Wed, 11 May 2022 04:02:27 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 04:02:27 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 04:02:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 04:02:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1b0318fd9d43e032add67ea408393c8e890c1ea4b437ecc600ea0107fa7de956`  
		Last Modified: Wed, 11 May 2022 02:11:56 GMT  
		Size: 19.4 MB (19359811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d6a8d215c465e56d8f308b31598d7cae73bef9a56e22a119d046b1440543d8`  
		Last Modified: Wed, 11 May 2022 04:03:24 GMT  
		Size: 5.8 MB (5780790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5a52e918af5f03a1416f801974f3730a5206537f17f46378fa67429c24e0ae`  
		Last Modified: Wed, 11 May 2022 04:05:05 GMT  
		Size: 35.3 MB (35291525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec39b317801752ad6eb2655215fa70797d5c161dd16caac8a031fa88926eb3c`  
		Last Modified: Wed, 11 May 2022 04:04:46 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c2a374c530fb20edb0d1039fa77753ae7f93f6921f8daabea00d8cb215d8c3`  
		Last Modified: Wed, 11 May 2022 04:04:46 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3911fdd86e9472e6f9bf5e0628aae4e9031d6fe8be9f792bd77383dd6ece0a`  
		Last Modified: Wed, 11 May 2022 04:04:46 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:14f815ef09eadcb495bc7686cd97aff68c0c327688f6a7bd91c967d04e7751dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61669454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8be3b5f87826c735222de2bcbfc1df70472048ba777023c05823b9bf5d856ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 11 May 2022 00:49:23 GMT
ADD file:2da23cbf134c6ddbf47e6a21fd94f5d08453f8ea5b6d8c101c8a55408e61162c in / 
# Wed, 11 May 2022 00:49:24 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:41:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 11 May 2022 01:42:26 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 11 May 2022 01:42:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 11 May 2022 01:42:36 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 11 May 2022 01:42:37 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 11 May 2022 01:42:37 GMT
EXPOSE 8888
# Wed, 11 May 2022 01:42:38 GMT
VOLUME [/var/lib/chronograf]
# Wed, 11 May 2022 01:42:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 11 May 2022 01:42:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 01:42:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:716cebb420f77090ed0f738eb4ff36a4aff63f4b8bd8ad1e9fa099b3e2a53961`  
		Last Modified: Wed, 11 May 2022 00:57:53 GMT  
		Size: 20.4 MB (20423950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cab351856977abcb6226f57f9fd6c6b26d48a8040da752d217bed7142cf58d7`  
		Last Modified: Wed, 11 May 2022 01:43:09 GMT  
		Size: 6.0 MB (6047083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad109811dad6305323b0c0483ec91a900e6119f794fa884188f958d56b22a5b`  
		Last Modified: Wed, 11 May 2022 01:43:57 GMT  
		Size: 35.2 MB (35174032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38515e26a218f5e1a76f36cdcbdb63cb6edf55c36da28becf537f0e3408dfdbe`  
		Last Modified: Wed, 11 May 2022 01:43:53 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07949b7bfb3ceabbf18d5db8f0640413eb00e8cb2c538b9ab9c942f1694e66d`  
		Last Modified: Wed, 11 May 2022 01:43:52 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acfe2694f6dc110bee371500c48c3ab959fb6e008449228f920548a56bbdefc`  
		Last Modified: Wed, 11 May 2022 01:43:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
