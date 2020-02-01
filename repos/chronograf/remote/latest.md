## `chronograf:latest`

```console
$ docker pull chronograf@sha256:ed41d4e0c2dc030d1fc8a109f79c6f710a3f692f693c5818af04a0077b118de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:50bcd319c808a7f9aa1986e53e89bebfcddb8e669fe05f075b8e0a4942aa9d26
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65396727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4ff2c46a5fd49e3e068226ea572382d2f9010d697d1bf92fe8db6bff75c3fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:22:40 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 04 Jan 2020 05:22:37 GMT
ENV CHRONOGRAF_VERSION=1.7.16
# Sat, 04 Jan 2020 05:22:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 04 Jan 2020 05:22:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 04 Jan 2020 05:22:50 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 04 Jan 2020 05:22:50 GMT
EXPOSE 8888
# Sat, 04 Jan 2020 05:22:50 GMT
VOLUME [/var/lib/chronograf]
# Sat, 04 Jan 2020 05:22:50 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 04 Jan 2020 05:22:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Jan 2020 05:22:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff78b833242a8d2f0e4b4a83472fdc141fbcc193e50e779802335a1e01908748`  
		Last Modified: Sat, 28 Dec 2019 08:24:26 GMT  
		Size: 4.5 MB (4503597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04224b2d6b88ab56aabea96d5ced5b8c972b9b5fb5d36099078309a24cc734fc`  
		Last Modified: Sat, 04 Jan 2020 05:23:16 GMT  
		Size: 38.3 MB (38344120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b3dfafa9c36ca3edfbdd1d72a3917d871e2abf821e4d7b0ff705e01051e74f`  
		Last Modified: Sat, 04 Jan 2020 05:23:10 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcc3fe6a9e8cc4c67dc22ca8910aa3f60595dec9b65e656eecd4c5ab1b7f7b2`  
		Last Modified: Sat, 04 Jan 2020 05:23:10 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc7a9809c66e4f3b375572049042fbe8aea12eacf839b91cc20cc0daccd1bd0`  
		Last Modified: Sat, 04 Jan 2020 05:23:10 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6329ff6d7821697751be5e271bca3eac84d112e2c66709ded61173ca70facede
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59013749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da0ef024bcfcc1831d413bc1eb4a84ab245a174a1a3e67e9c5f17d0ec764807`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:41:53 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 01 Feb 2020 18:43:14 GMT
ENV CHRONOGRAF_VERSION=1.7.16
# Sat, 01 Feb 2020 18:43:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 01 Feb 2020 18:43:37 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 01 Feb 2020 18:43:37 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 01 Feb 2020 18:43:38 GMT
EXPOSE 8888
# Sat, 01 Feb 2020 18:43:39 GMT
VOLUME [/var/lib/chronograf]
# Sat, 01 Feb 2020 18:43:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 01 Feb 2020 18:43:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 18:43:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f767a4ddc4b77052dac2b0b69478ffb671116744c71e02d18133e277dd7c19d`  
		Last Modified: Sat, 01 Feb 2020 18:43:54 GMT  
		Size: 3.9 MB (3877381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611f132eaa9e78a937d09163db434cc699ec850c6a956b60e114e3d06645cf82`  
		Last Modified: Sat, 01 Feb 2020 18:44:32 GMT  
		Size: 35.8 MB (35800350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aec15abccca3cd4183e9a6690bf71a96344a183d62977fabb35230d2c232645`  
		Last Modified: Sat, 01 Feb 2020 18:44:22 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261c04826686c1e1dcbaaed0141369d992cca8524a67f58ddaab9ad9ac4bafd2`  
		Last Modified: Sat, 01 Feb 2020 18:44:22 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e4d3bf6b962bdb74b686bdb3d745a1d8096f91d39bd46319d74ee428446d82`  
		Last Modified: Sat, 01 Feb 2020 18:44:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2056ecca879b1a80688e00935b249d0c82b4f4d6b8fff6a9a66edd15e5af31c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60494364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2cd148be0d67747a943e380102c88ecb9185be7bb4dbcd1caa79fd66de7bd5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:53:12 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 01 Feb 2020 17:54:21 GMT
ENV CHRONOGRAF_VERSION=1.7.16
# Sat, 01 Feb 2020 17:54:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 01 Feb 2020 17:54:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 01 Feb 2020 17:55:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 01 Feb 2020 17:55:01 GMT
EXPOSE 8888
# Sat, 01 Feb 2020 17:55:02 GMT
VOLUME [/var/lib/chronograf]
# Sat, 01 Feb 2020 17:55:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 01 Feb 2020 17:55:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 17:55:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb406db3a5bf4f487242b44b5eb117d90608bc16921e74ddf810f1e61cfc5a3c`  
		Last Modified: Sat, 01 Feb 2020 17:55:22 GMT  
		Size: 4.1 MB (4080784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ba1ebc98538ba96dd45ca27832a6d39a58f164cc7182edbc00154dbd946055`  
		Last Modified: Sat, 01 Feb 2020 17:56:03 GMT  
		Size: 36.0 MB (36003332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744e9d474940294854c8ea2446dce84039f5457247c5c97e5d67c56207513392`  
		Last Modified: Sat, 01 Feb 2020 17:55:55 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba7e7c977114fc1347004bcc5ef6f4a3218dd40b400e91b850db2ef1523fb2b`  
		Last Modified: Sat, 01 Feb 2020 17:55:55 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a86840da3d471928b27a8641246e91b07fc74a29be58318e76c5ff84535886a`  
		Last Modified: Sat, 01 Feb 2020 17:55:55 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
