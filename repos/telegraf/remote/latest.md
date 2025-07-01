## `telegraf:latest`

```console
$ docker pull telegraf@sha256:72f89db927431152af0d2aa61d9462dbc0913e4eab10193ab320e1de824f73ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:794857af3bfca93a8bb37c9d014da9aa4d42f867c217f9ab42a9b18e2251cda0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169934969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56407da986d0a6d13a51524f13c4a663499105dc0b5397b17afe4807fe3d9654`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72864e4928e35ff6c6b6e3e7aa816ee1b5f3fb618baaf2008ac865a34795926b`  
		Last Modified: Tue, 01 Jul 2025 03:26:38 GMT  
		Size: 18.9 MB (18946627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4eb62bea469c40ed112705779da59c026d8820bb81decb16912a5f7ca62cb6`  
		Last Modified: Tue, 01 Jul 2025 03:26:37 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de9ae5617fe32c7cbe7ffd1f1a3e43b37dffdb8bc7f6656e5e05f84b893a070`  
		Last Modified: Tue, 01 Jul 2025 03:26:46 GMT  
		Size: 78.5 MB (78470962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e475bea97f877cf09cd3ae2a132fb274e947e03baea4764b26d24b139526d1`  
		Last Modified: Tue, 01 Jul 2025 03:26:37 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:c25bb14a0abf2568f1b674b6cd3e8e1dcb0c4ee042356d740dadef6906e97d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6653216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80bd367ebb493ba94afbe5ac1ad1f798b550a32c3a4a0b156c35fdc26adf678`

```dockerfile
```

-	Layers:
	-	`sha256:fae96db7acc750044041ca25da5ce670b8f940272ed9f65b07dfdae55fb281e7`  
		Last Modified: Tue, 01 Jul 2025 06:10:33 GMT  
		Size: 6.6 MB (6638445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b00ccb6d978f64a7ed3887955d927efbbfea90c8d8a664c8865dafa16db3460a`  
		Last Modified: Tue, 01 Jul 2025 06:10:34 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:cded87ca8cb59cd91711d01580187bc2c5b36f690173f40cb2df34a575bf9577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156374353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715302f7358dee1774cc082629800a737507d6cfcdfec11b08b149db429507d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bc2e28ca8cdb751a10e1e014b374d783cdfa924e032e1f9eb674e7fae1220927`  
		Last Modified: Tue, 01 Jul 2025 01:14:29 GMT  
		Size: 44.2 MB (44208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcc606b1195a348c6a47399c1a54ab936d4477a526d62306ddce89fe76a2d22`  
		Last Modified: Tue, 01 Jul 2025 08:59:56 GMT  
		Size: 21.9 MB (21928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c302fde068c863419c2c44c2bc8a839273313323f89cfd808efde87f6fa2a944`  
		Last Modified: Tue, 01 Jul 2025 20:35:57 GMT  
		Size: 17.7 MB (17724911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b78da67c92f5fb72d38666bc079b283625e8c5007656b200ebc00a4e07e318`  
		Last Modified: Tue, 01 Jul 2025 20:35:57 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e0b4a33ab63af973072d3a0713e873b37dcc089b6cf633d3eed1ad0e1b0cf4`  
		Last Modified: Tue, 01 Jul 2025 20:37:33 GMT  
		Size: 72.5 MB (72510520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d2e2115c2bd5295fd8dd6aa853e84e1a557e69c75bb45319abbd37f0aac988`  
		Last Modified: Tue, 01 Jul 2025 20:37:28 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:940054b1b8795b1ac2ba4a5af27d2299a9554d1d97abf0bec485fad9e5541c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6647914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a78697dde22e64e507f7be4627ec6380edaac6cd40b23fddd67459bbfea71eb`

```dockerfile
```

-	Layers:
	-	`sha256:de44d2fe9e715a1c5de75a3e553d0d4af54629e62ca8b59929b593fe1f431938`  
		Last Modified: Tue, 01 Jul 2025 21:10:37 GMT  
		Size: 6.6 MB (6633048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1ee05d990f80957d59f678bc04a412503ace9c6790d3272b1d1e774fcc15e3`  
		Last Modified: Tue, 01 Jul 2025 21:10:38 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3f78f10296766c7e96f9834ba8b59005134b41d58edcc5c8e592ef36b1930eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161920784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f9e91d82b72aa0626f8f7b17e553f688860152e385db6af87ea0c31894b82c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20800ae39e9ca2bb820c115b99be542e5f39ca467f193f30e7fd9a46f8dcd1`  
		Last Modified: Tue, 01 Jul 2025 16:15:11 GMT  
		Size: 18.9 MB (18871971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374df1ae81d67b566dd34a7e801fcb18d41b8f6692da11a76dd0148e5f3407bd`  
		Last Modified: Tue, 01 Jul 2025 16:15:09 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6239b80a6fd714d01d53c33ea2e75cf4358aa05155e472e977b7de0c7f1f92`  
		Last Modified: Tue, 01 Jul 2025 17:12:41 GMT  
		Size: 71.1 MB (71149612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9cdc3b2cc79e594f2517d3e1ad5fbf8126d8ec127535abf448f5993e4e78d6`  
		Last Modified: Tue, 01 Jul 2025 16:19:04 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:0e8407e8a88751332dd332467adf069c614459b1660eca8e053f895e69e2eb7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6654026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659fdd9596578830604e7bdcca59b11c341ec064e9cf5c3f00dbd4307a14d8f8`

```dockerfile
```

-	Layers:
	-	`sha256:9ec808672276a92b0aa293e5884d2a477846f4f642f9fceca17927a39d5eb5b3`  
		Last Modified: Tue, 01 Jul 2025 18:10:41 GMT  
		Size: 6.6 MB (6639133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c922348195ca06e280093d41bf314cefad72b2c942994785fab74dc2837c66e5`  
		Last Modified: Tue, 01 Jul 2025 18:10:42 GMT  
		Size: 14.9 KB (14893 bytes)  
		MIME: application/vnd.in-toto+json
