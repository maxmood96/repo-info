<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.29`](#telegraf129)
-	[`telegraf:1.29-alpine`](#telegraf129-alpine)
-	[`telegraf:1.29.5`](#telegraf1295)
-	[`telegraf:1.29.5-alpine`](#telegraf1295-alpine)
-	[`telegraf:1.30`](#telegraf130)
-	[`telegraf:1.30-alpine`](#telegraf130-alpine)
-	[`telegraf:1.30.3`](#telegraf1303)
-	[`telegraf:1.30.3-alpine`](#telegraf1303-alpine)
-	[`telegraf:1.31`](#telegraf131)
-	[`telegraf:1.31-alpine`](#telegraf131-alpine)
-	[`telegraf:1.31.3`](#telegraf1313)
-	[`telegraf:1.31.3-alpine`](#telegraf1313-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.29`

```console
$ docker pull telegraf@sha256:7bba2d53bd85c08f88bc39ee9496b848ff051c9b8d1529457aa3faecc1b61206
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29` - linux; amd64

```console
$ docker pull telegraf@sha256:ea87b190a132e4579110c81f25b90137a0b66993b3926a99f63132548f5a089f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155197596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7596b3984b3fa8ec230486445bfab1df744f9c03c16b1fe7deaf3b0ececd86b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021f62b88754979f246ce9cc16cf35c38314900adf59064b68279df958c135a`  
		Last Modified: Tue, 13 Aug 2024 02:06:49 GMT  
		Size: 18.9 MB (18947967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6eafa0fd6f755e5f565236a06c0324267dfc268c562108392ed38b2652ae79`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59117e331826cf2a0ec36961df1532875fe016497859b27948808eafb373ad58`  
		Last Modified: Tue, 13 Aug 2024 02:06:50 GMT  
		Size: 62.6 MB (62642454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6619767ff0a0354bb7dce4c0e71f1593be1f50f66b56a2e57f358a9d8c29db0`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:eb920af66653c8edd9b36d76b317fcd38895fa6d2dc9fadff13791fece36f4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901cc2ef43539b3c67ae6fb5f703622c52bd92569e84450ffc1bd125491506fe`

```dockerfile
```

-	Layers:
	-	`sha256:55baa24c21639a28c4c390561d56605ff0ddf5d47508b5acd306c9af2d30d177`  
		Last Modified: Tue, 13 Aug 2024 02:06:49 GMT  
		Size: 6.4 MB (6391317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeb993520d6e5904931855872d554e3a275587b3d94aaca33073c261356bc17b`  
		Last Modified: Tue, 13 Aug 2024 02:06:49 GMT  
		Size: 14.3 KB (14323 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:96c3783d79e55205bef7e9fae322965de333f079b11cbbb218b21b6e70c2d425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142815036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c87f4c597d3ff737c337436ae875b844033e9d1657eb18f90d820f1ea3adc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Jul 2024 16:07:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf87fb7435f010785c8132726eefe29fb6076e5a51a7bbf617fee5b66e8dd893`  
		Last Modified: Wed, 24 Jul 2024 14:45:16 GMT  
		Size: 17.7 MB (17724878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157c36a5580cef7adf1606a141f5825bbc1cbbde1c1c857f4abeec3e2f4f2ed6`  
		Last Modified: Wed, 24 Jul 2024 14:45:16 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce54b45e55ad570865956e2b97ef84a9db5a8b6b60ea134f13af74302fdbc68`  
		Last Modified: Wed, 24 Jul 2024 14:45:18 GMT  
		Size: 58.0 MB (57984968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdca7eefa237d5827b0c0ba113e294104a34ddb2f9eca9c2c1f26547ea5ce9ba`  
		Last Modified: Wed, 24 Jul 2024 14:45:16 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:07183705d90435555242c438f9b1aaa182ab4cea7aa3ce821aa1c41ca38e0b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6feead37d6d564cb480823ff703c38b0175a2e688566f565a6639124d0ea6cc0`

```dockerfile
```

-	Layers:
	-	`sha256:db6885bb374bf855666ebda24772c5d453750d420f703d71f4606ce8348040d7`  
		Last Modified: Wed, 24 Jul 2024 14:45:16 GMT  
		Size: 6.4 MB (6385958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50137ec048b786972077982f326b63622e67bab85e3f656dcd7e23fdf28b2550`  
		Last Modified: Wed, 24 Jul 2024 14:45:15 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:1b051a4db44d8da595c15d85c348f64bb9e38fcf50f59ef7e9e528cdf589783b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149034746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f485b5a1f19de21e2557b65bf5804d4cbe3788bba57be8459ec48badd0d860`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2fd1362c98163030a52de79cafd3d14c1f56f0cbf2522eeab2c7845e36f421`  
		Last Modified: Tue, 13 Aug 2024 19:50:31 GMT  
		Size: 18.9 MB (18870195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90d8eb9c97f62b179fa41c54488c4a5099ad2be872c140f1e01b9e997ad71cf`  
		Last Modified: Tue, 13 Aug 2024 19:50:30 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73eb0a1a0b82b6775fb619d7dcb702732c99286a18ccd39186605ceef4d75de`  
		Last Modified: Tue, 13 Aug 2024 19:50:32 GMT  
		Size: 57.0 MB (56981120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf7ecffcba92e2fcd8804dc60d509f12ffafb32067468a4286f88a0df1ac493`  
		Last Modified: Tue, 13 Aug 2024 19:50:30 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:211d8963b0c36490f62727f04a86cfb4f30c02ca19b8d056c73af84c3aba681f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81cb2c0290f4a27d5121dbbe3382ec1b37f7e2a08680243adf6a70ad3cee3db`

```dockerfile
```

-	Layers:
	-	`sha256:06f4dcbd53049b41b02f2987a5787397bb28a1ddc5aa11856738ea20985542cd`  
		Last Modified: Tue, 13 Aug 2024 19:50:30 GMT  
		Size: 6.4 MB (6391240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbe3bc3b46e7e7c45ba8dac85040432d7a0ed5d6d4611f57ee6a27b055404b0e`  
		Last Modified: Tue, 13 Aug 2024 19:50:30 GMT  
		Size: 14.6 KB (14617 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29-alpine`

```console
$ docker pull telegraf@sha256:b1c2e442428e68f8879f094076237a8d71f9a7e1a569c992bf8c21069e443b18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:49f29125ad9233ff1bc5ea54024c4efd28e29a49e1b23b5e7108bb1130d32ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68516735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219c44bf7f97fbf6ec80259f34fc86d159a99275fe3aa51cccd8f6355de27764`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4132a9248b477c331526d071bc59ada3e5507ba7aa74b153a06aedf97735e3`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73efbc3eb4ae808763b36076a63493b677491ee7c62252fe659f77104dfbbd4`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 2.5 MB (2451692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37a936729a8ef51dea490c7ccb55de9eda7ea83a4a113c02f3f1eb4385f720f`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 62.4 MB (62441543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477c74b92f0f8849341c14b2292bc23755c4502d83f34369eb10f1f4550fec1d`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6f6e7b879e0e5bb41f6b43fb96aba99b8f3fe0398eb21426b85f02894332d281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1070504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4313fc3bf11bea29cee746e976c05d01de6caf9ca84c3f1e00a0e624887eb9`

```dockerfile
```

-	Layers:
	-	`sha256:200f9fb6ad3db368b251ba2339e4d956660225bc79c8a2208cea7e4984dafba9`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 1.1 MB (1055772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d263f2e91dc9c2336bd7ff18be122ca6af9fbae249c5b699921156bacccb2d`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 14.7 KB (14732 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5da5aa4566fb2bfd24bb52fff8400f836598193e97f0d3750c026498997cf86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63405473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c24924333978c8c70a609fc3c6223677e132506a48b6fc6a655714badb71f8b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da0d1ffb94d496286226e500ca461ae4c84a6368b8c23b64dfd72955579f654`  
		Last Modified: Wed, 24 Jul 2024 10:08:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c96666ef40bebea34c4984a3d34ddd3118468eb0087d117403688b0408735f6`  
		Last Modified: Wed, 24 Jul 2024 10:08:09 GMT  
		Size: 2.5 MB (2537424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0e59cfe1707ecb5ecfec7c63696c917ee3ed8bd002d14d40aa6866e4abce57`  
		Last Modified: Wed, 24 Jul 2024 10:08:11 GMT  
		Size: 56.8 MB (56780507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f633c760e44ef0d1301c842ab06c7fe9e073fd9e44e9448323f6d8cc98c7e728`  
		Last Modified: Wed, 24 Jul 2024 10:08:08 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a19d2a7abcbe8fd4629bb91327edf9a69c41b23c49d1427b0ad8b3ec4b8fbabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1065651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b44f66460c3f5d9f8e20199bfda71fc87a3a256aa99f5146bd57fab863a8ab`

```dockerfile
```

-	Layers:
	-	`sha256:22c9cf8034785d65d1a08b743b8e27ce19acbec3f2b40a3fed684e6dc32fd0db`  
		Last Modified: Wed, 24 Jul 2024 10:08:09 GMT  
		Size: 1.1 MB (1050642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aad42f4d45df4450467ae8babb9e22d7018e72959826948ba41db26d5b13a00`  
		Last Modified: Wed, 24 Jul 2024 10:08:08 GMT  
		Size: 15.0 KB (15009 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29.5`

```console
$ docker pull telegraf@sha256:7bba2d53bd85c08f88bc39ee9496b848ff051c9b8d1529457aa3faecc1b61206
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29.5` - linux; amd64

```console
$ docker pull telegraf@sha256:ea87b190a132e4579110c81f25b90137a0b66993b3926a99f63132548f5a089f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155197596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7596b3984b3fa8ec230486445bfab1df744f9c03c16b1fe7deaf3b0ececd86b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021f62b88754979f246ce9cc16cf35c38314900adf59064b68279df958c135a`  
		Last Modified: Tue, 13 Aug 2024 02:06:49 GMT  
		Size: 18.9 MB (18947967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6eafa0fd6f755e5f565236a06c0324267dfc268c562108392ed38b2652ae79`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59117e331826cf2a0ec36961df1532875fe016497859b27948808eafb373ad58`  
		Last Modified: Tue, 13 Aug 2024 02:06:50 GMT  
		Size: 62.6 MB (62642454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6619767ff0a0354bb7dce4c0e71f1593be1f50f66b56a2e57f358a9d8c29db0`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:eb920af66653c8edd9b36d76b317fcd38895fa6d2dc9fadff13791fece36f4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901cc2ef43539b3c67ae6fb5f703622c52bd92569e84450ffc1bd125491506fe`

```dockerfile
```

-	Layers:
	-	`sha256:55baa24c21639a28c4c390561d56605ff0ddf5d47508b5acd306c9af2d30d177`  
		Last Modified: Tue, 13 Aug 2024 02:06:49 GMT  
		Size: 6.4 MB (6391317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeb993520d6e5904931855872d554e3a275587b3d94aaca33073c261356bc17b`  
		Last Modified: Tue, 13 Aug 2024 02:06:49 GMT  
		Size: 14.3 KB (14323 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29.5` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:96c3783d79e55205bef7e9fae322965de333f079b11cbbb218b21b6e70c2d425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142815036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c87f4c597d3ff737c337436ae875b844033e9d1657eb18f90d820f1ea3adc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Jul 2024 16:07:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf87fb7435f010785c8132726eefe29fb6076e5a51a7bbf617fee5b66e8dd893`  
		Last Modified: Wed, 24 Jul 2024 14:45:16 GMT  
		Size: 17.7 MB (17724878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157c36a5580cef7adf1606a141f5825bbc1cbbde1c1c857f4abeec3e2f4f2ed6`  
		Last Modified: Wed, 24 Jul 2024 14:45:16 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce54b45e55ad570865956e2b97ef84a9db5a8b6b60ea134f13af74302fdbc68`  
		Last Modified: Wed, 24 Jul 2024 14:45:18 GMT  
		Size: 58.0 MB (57984968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdca7eefa237d5827b0c0ba113e294104a34ddb2f9eca9c2c1f26547ea5ce9ba`  
		Last Modified: Wed, 24 Jul 2024 14:45:16 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:07183705d90435555242c438f9b1aaa182ab4cea7aa3ce821aa1c41ca38e0b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6feead37d6d564cb480823ff703c38b0175a2e688566f565a6639124d0ea6cc0`

```dockerfile
```

-	Layers:
	-	`sha256:db6885bb374bf855666ebda24772c5d453750d420f703d71f4606ce8348040d7`  
		Last Modified: Wed, 24 Jul 2024 14:45:16 GMT  
		Size: 6.4 MB (6385958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50137ec048b786972077982f326b63622e67bab85e3f656dcd7e23fdf28b2550`  
		Last Modified: Wed, 24 Jul 2024 14:45:15 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:1b051a4db44d8da595c15d85c348f64bb9e38fcf50f59ef7e9e528cdf589783b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149034746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f485b5a1f19de21e2557b65bf5804d4cbe3788bba57be8459ec48badd0d860`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2fd1362c98163030a52de79cafd3d14c1f56f0cbf2522eeab2c7845e36f421`  
		Last Modified: Tue, 13 Aug 2024 19:50:31 GMT  
		Size: 18.9 MB (18870195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90d8eb9c97f62b179fa41c54488c4a5099ad2be872c140f1e01b9e997ad71cf`  
		Last Modified: Tue, 13 Aug 2024 19:50:30 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73eb0a1a0b82b6775fb619d7dcb702732c99286a18ccd39186605ceef4d75de`  
		Last Modified: Tue, 13 Aug 2024 19:50:32 GMT  
		Size: 57.0 MB (56981120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf7ecffcba92e2fcd8804dc60d509f12ffafb32067468a4286f88a0df1ac493`  
		Last Modified: Tue, 13 Aug 2024 19:50:30 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:211d8963b0c36490f62727f04a86cfb4f30c02ca19b8d056c73af84c3aba681f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81cb2c0290f4a27d5121dbbe3382ec1b37f7e2a08680243adf6a70ad3cee3db`

```dockerfile
```

-	Layers:
	-	`sha256:06f4dcbd53049b41b02f2987a5787397bb28a1ddc5aa11856738ea20985542cd`  
		Last Modified: Tue, 13 Aug 2024 19:50:30 GMT  
		Size: 6.4 MB (6391240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbe3bc3b46e7e7c45ba8dac85040432d7a0ed5d6d4611f57ee6a27b055404b0e`  
		Last Modified: Tue, 13 Aug 2024 19:50:30 GMT  
		Size: 14.6 KB (14617 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.29.5-alpine`

```console
$ docker pull telegraf@sha256:b1c2e442428e68f8879f094076237a8d71f9a7e1a569c992bf8c21069e443b18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.29.5-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:49f29125ad9233ff1bc5ea54024c4efd28e29a49e1b23b5e7108bb1130d32ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68516735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219c44bf7f97fbf6ec80259f34fc86d159a99275fe3aa51cccd8f6355de27764`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4132a9248b477c331526d071bc59ada3e5507ba7aa74b153a06aedf97735e3`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73efbc3eb4ae808763b36076a63493b677491ee7c62252fe659f77104dfbbd4`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 2.5 MB (2451692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37a936729a8ef51dea490c7ccb55de9eda7ea83a4a113c02f3f1eb4385f720f`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 62.4 MB (62441543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477c74b92f0f8849341c14b2292bc23755c4502d83f34369eb10f1f4550fec1d`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6f6e7b879e0e5bb41f6b43fb96aba99b8f3fe0398eb21426b85f02894332d281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1070504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4313fc3bf11bea29cee746e976c05d01de6caf9ca84c3f1e00a0e624887eb9`

```dockerfile
```

-	Layers:
	-	`sha256:200f9fb6ad3db368b251ba2339e4d956660225bc79c8a2208cea7e4984dafba9`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 1.1 MB (1055772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d263f2e91dc9c2336bd7ff18be122ca6af9fbae249c5b699921156bacccb2d`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 14.7 KB (14732 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.29.5-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5da5aa4566fb2bfd24bb52fff8400f836598193e97f0d3750c026498997cf86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63405473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c24924333978c8c70a609fc3c6223677e132506a48b6fc6a655714badb71f8b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.29.5
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da0d1ffb94d496286226e500ca461ae4c84a6368b8c23b64dfd72955579f654`  
		Last Modified: Wed, 24 Jul 2024 10:08:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c96666ef40bebea34c4984a3d34ddd3118468eb0087d117403688b0408735f6`  
		Last Modified: Wed, 24 Jul 2024 10:08:09 GMT  
		Size: 2.5 MB (2537424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0e59cfe1707ecb5ecfec7c63696c917ee3ed8bd002d14d40aa6866e4abce57`  
		Last Modified: Wed, 24 Jul 2024 10:08:11 GMT  
		Size: 56.8 MB (56780507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f633c760e44ef0d1301c842ab06c7fe9e073fd9e44e9448323f6d8cc98c7e728`  
		Last Modified: Wed, 24 Jul 2024 10:08:08 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a19d2a7abcbe8fd4629bb91327edf9a69c41b23c49d1427b0ad8b3ec4b8fbabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1065651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b44f66460c3f5d9f8e20199bfda71fc87a3a256aa99f5146bd57fab863a8ab`

```dockerfile
```

-	Layers:
	-	`sha256:22c9cf8034785d65d1a08b743b8e27ce19acbec3f2b40a3fed684e6dc32fd0db`  
		Last Modified: Wed, 24 Jul 2024 10:08:09 GMT  
		Size: 1.1 MB (1050642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aad42f4d45df4450467ae8babb9e22d7018e72959826948ba41db26d5b13a00`  
		Last Modified: Wed, 24 Jul 2024 10:08:08 GMT  
		Size: 15.0 KB (15009 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30`

```console
$ docker pull telegraf@sha256:81a75c27f4899de17fc0bb30efaa4a096073a127d4ee20f2d2cab43e11ded516
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30` - linux; amd64

```console
$ docker pull telegraf@sha256:105baac2846a58764ea7b29b03d4fe9a64a5fd7f971bd1f56398adbdaa76d769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155321578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07643c3563aba7f88f73ce53fb6dd92eb2daa22fd744b9234a9d40e19385c8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d202b5d1028872249f5bdac9b2bf6304178492371eda7a5bf3656a34adb8495e`  
		Last Modified: Tue, 13 Aug 2024 02:06:43 GMT  
		Size: 18.9 MB (18947930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddba2633967017c8581bd38be4e8a9dd19d361a96c1a5c0255ee25bf6c0548ea`  
		Last Modified: Tue, 13 Aug 2024 02:06:43 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88ff29ce79000dcd23f8c4af6c76e610420bc2b84135ff3df13f179d9c9136`  
		Last Modified: Tue, 13 Aug 2024 02:06:44 GMT  
		Size: 62.8 MB (62766458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ce46e790e452b486a658fe055edefeb75176f17c2f8e6f1fe63d51aab609c`  
		Last Modified: Tue, 13 Aug 2024 02:06:44 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:2a96754b3e0e8e633c95b048bc5819b4c7ef611cece56ce752595605ef879017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6406064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c4f0868362df80617bcb8a4473968968d52cd215bc86b12770c4621bea892b`

```dockerfile
```

-	Layers:
	-	`sha256:1e51abd6afc0fe4f41d7b08c0261ebf89cc7e3bbf07230a78728bf6f253c63ef`  
		Last Modified: Tue, 13 Aug 2024 02:06:43 GMT  
		Size: 6.4 MB (6391740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d414dd262d0b77c76f2b5d96cfaf9450ff6dfce8ba3b6d02055d8b530f3fda94`  
		Last Modified: Tue, 13 Aug 2024 02:06:43 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:0bf005138526a6d7f89f622fbab2a3074121083de1945c7163786f3b88e153b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143042726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366320f5e94cf54b295b059a55f78f5c94913f7ff4a0dc3ca41cd39213e597b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Jul 2024 16:07:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf87fb7435f010785c8132726eefe29fb6076e5a51a7bbf617fee5b66e8dd893`  
		Last Modified: Wed, 24 Jul 2024 14:45:16 GMT  
		Size: 17.7 MB (17724878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157c36a5580cef7adf1606a141f5825bbc1cbbde1c1c857f4abeec3e2f4f2ed6`  
		Last Modified: Wed, 24 Jul 2024 14:45:16 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab57d18cde6e39fb860d405c8f7556a68f11072131a75860e27e38a32f8f224`  
		Last Modified: Wed, 24 Jul 2024 14:46:09 GMT  
		Size: 58.2 MB (58212658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74611a17908cf3eab9198acdc519f3e990adfc05cdfcf6eac55288fac0e915b9`  
		Last Modified: Wed, 24 Jul 2024 14:46:07 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:50d83a10ef1745dcebfc3e00c978385fadb1a2666365f06ce1c8cc788132cf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8487462b8522702ae7c5eba12c370ddc5a9f6e620b9b5469151f958f0390a8c`

```dockerfile
```

-	Layers:
	-	`sha256:dcdb3d8ac7a0180c710ff5f320266b3675307a76d43c648b83cd263d846d7f6d`  
		Last Modified: Wed, 24 Jul 2024 14:46:07 GMT  
		Size: 6.4 MB (6386381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17b9ccd98f4231b7162ab9a5e9eadb31d85ad4de3fe64de93570585a0b1c9622`  
		Last Modified: Wed, 24 Jul 2024 14:46:07 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c15ea28bde73880ab7f94027b9c05e2d4620a858958d672fd878ab8f5082364b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149176881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eee13f728fdf4dc2d94ef984aa65311be7fd3bf0d4f2441d60a1aa86bc9d41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2fd1362c98163030a52de79cafd3d14c1f56f0cbf2522eeab2c7845e36f421`  
		Last Modified: Tue, 13 Aug 2024 19:50:31 GMT  
		Size: 18.9 MB (18870195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90d8eb9c97f62b179fa41c54488c4a5099ad2be872c140f1e01b9e997ad71cf`  
		Last Modified: Tue, 13 Aug 2024 19:50:30 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30016fc60948562533654a15dd52496feada8d17a364f3fba24081990a51f93f`  
		Last Modified: Tue, 13 Aug 2024 19:51:05 GMT  
		Size: 57.1 MB (57123255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe90c4c1e966be3deeaf6987962b52e903fed2d1f08748d8372ccb3d9c1c2cdf`  
		Last Modified: Tue, 13 Aug 2024 19:51:03 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:10431b688df6bc8f1f01f64a4a6d1bdfd9ad1b4eb2203fce623956dba0f0921b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6406279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f6f99d2da727b90404a73202844b8ea710318690b3b9c8c04abee5f1f470d3`

```dockerfile
```

-	Layers:
	-	`sha256:0bd97d302fcee6750f95274d52513e2e7a30519eef63476d6c835b71c30cdec9`  
		Last Modified: Tue, 13 Aug 2024 19:51:04 GMT  
		Size: 6.4 MB (6391663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cef20fb611517b3a889bc0268cfbf4c86cab491e3913c7e9ded4bb88a22b709`  
		Last Modified: Tue, 13 Aug 2024 19:51:03 GMT  
		Size: 14.6 KB (14616 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30-alpine`

```console
$ docker pull telegraf@sha256:97bb530cc385132152f0f171db0514dd3b852d6f1529f135de0d1c3ed4a64805
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:fcfe5222366ad62f02e065f1a69e45bce3bdc64e7cc6bcc20dd5f5ea12eb3977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68644019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242ce2c4f74738cd111a37d48992142573863a657f5421e6429e62662fe350da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc469e64f8855e42c6d4c6f121d649ce80b1b57b520030009bdb799aaf7b6d3`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd1dd2aea95e4d6aaeb5eadb1505da9fa8ba75ed038b99116d1289d3ee3607e`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 2.5 MB (2451682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da5b95773c156c402ef1eaaf6796f414895775753500372be983f0dc9d1d0ad`  
		Last Modified: Mon, 22 Jul 2024 23:04:34 GMT  
		Size: 62.6 MB (62568841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32432b32d0336088c3d13e71d5f2557b2fec10426fcfbd387f37801d9a94865b`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6e5a535211e37ba0525e30ae5b7005cffd5005998e7ce1cfaed15f200eeffd88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1070929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043244b274180f906f2a190fa8d7d09cbe1b5019f3de0040c8cfff6cf38cdc49`

```dockerfile
```

-	Layers:
	-	`sha256:47672bde33a0416036b3df7aa8668fc62f2d1b877370d59b5ca3a9e1118e1e0d`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 1.1 MB (1056195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3753d4298e51b5ffd45bfc070c77a5b4f56235122d929b090b405de0e4fd9aa`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:75a9c7f73eedd98dc2b6a64d5e280a846580396dbf9beb921d86e186cd328313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63545852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e783d7f3d1a9a6923de67a97257eb420d2f5a3363f798f2c3bb1eedff90488`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da0d1ffb94d496286226e500ca461ae4c84a6368b8c23b64dfd72955579f654`  
		Last Modified: Wed, 24 Jul 2024 10:08:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c96666ef40bebea34c4984a3d34ddd3118468eb0087d117403688b0408735f6`  
		Last Modified: Wed, 24 Jul 2024 10:08:09 GMT  
		Size: 2.5 MB (2537424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e8a5942cbf5e0ef4d4255f119ce9d09d2c12a398538968aa5e78e2776d217a`  
		Last Modified: Wed, 24 Jul 2024 10:09:20 GMT  
		Size: 56.9 MB (56920887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474ac264b7008a9fabe6524487bd7bf820471fcb7bb5c600987ec44467b4d449`  
		Last Modified: Wed, 24 Jul 2024 10:09:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f9f7a61706ac67a335a92fa5448f8686290e0c1ce3689a186a08b620e16b3391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1066074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3486c7c0fa924d31507d7209b6055436fa9328a1f9bc101377f671ab00066071`

```dockerfile
```

-	Layers:
	-	`sha256:42bff7dffe23c1a81e044f9a8c3f5d35be7f93cba815e4da644691450f121e3a`  
		Last Modified: Wed, 24 Jul 2024 10:09:19 GMT  
		Size: 1.1 MB (1051065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d0280828ab5dc2c7606151e8005b003e9dd82e13f11311ad0775a53fc7161d`  
		Last Modified: Wed, 24 Jul 2024 10:09:18 GMT  
		Size: 15.0 KB (15009 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.3`

```console
$ docker pull telegraf@sha256:81a75c27f4899de17fc0bb30efaa4a096073a127d4ee20f2d2cab43e11ded516
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30.3` - linux; amd64

```console
$ docker pull telegraf@sha256:105baac2846a58764ea7b29b03d4fe9a64a5fd7f971bd1f56398adbdaa76d769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155321578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07643c3563aba7f88f73ce53fb6dd92eb2daa22fd744b9234a9d40e19385c8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d202b5d1028872249f5bdac9b2bf6304178492371eda7a5bf3656a34adb8495e`  
		Last Modified: Tue, 13 Aug 2024 02:06:43 GMT  
		Size: 18.9 MB (18947930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddba2633967017c8581bd38be4e8a9dd19d361a96c1a5c0255ee25bf6c0548ea`  
		Last Modified: Tue, 13 Aug 2024 02:06:43 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88ff29ce79000dcd23f8c4af6c76e610420bc2b84135ff3df13f179d9c9136`  
		Last Modified: Tue, 13 Aug 2024 02:06:44 GMT  
		Size: 62.8 MB (62766458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07ce46e790e452b486a658fe055edefeb75176f17c2f8e6f1fe63d51aab609c`  
		Last Modified: Tue, 13 Aug 2024 02:06:44 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:2a96754b3e0e8e633c95b048bc5819b4c7ef611cece56ce752595605ef879017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6406064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c4f0868362df80617bcb8a4473968968d52cd215bc86b12770c4621bea892b`

```dockerfile
```

-	Layers:
	-	`sha256:1e51abd6afc0fe4f41d7b08c0261ebf89cc7e3bbf07230a78728bf6f253c63ef`  
		Last Modified: Tue, 13 Aug 2024 02:06:43 GMT  
		Size: 6.4 MB (6391740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d414dd262d0b77c76f2b5d96cfaf9450ff6dfce8ba3b6d02055d8b530f3fda94`  
		Last Modified: Tue, 13 Aug 2024 02:06:43 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:0bf005138526a6d7f89f622fbab2a3074121083de1945c7163786f3b88e153b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143042726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366320f5e94cf54b295b059a55f78f5c94913f7ff4a0dc3ca41cd39213e597b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Jul 2024 16:07:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf87fb7435f010785c8132726eefe29fb6076e5a51a7bbf617fee5b66e8dd893`  
		Last Modified: Wed, 24 Jul 2024 14:45:16 GMT  
		Size: 17.7 MB (17724878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157c36a5580cef7adf1606a141f5825bbc1cbbde1c1c857f4abeec3e2f4f2ed6`  
		Last Modified: Wed, 24 Jul 2024 14:45:16 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab57d18cde6e39fb860d405c8f7556a68f11072131a75860e27e38a32f8f224`  
		Last Modified: Wed, 24 Jul 2024 14:46:09 GMT  
		Size: 58.2 MB (58212658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74611a17908cf3eab9198acdc519f3e990adfc05cdfcf6eac55288fac0e915b9`  
		Last Modified: Wed, 24 Jul 2024 14:46:07 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:50d83a10ef1745dcebfc3e00c978385fadb1a2666365f06ce1c8cc788132cf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8487462b8522702ae7c5eba12c370ddc5a9f6e620b9b5469151f958f0390a8c`

```dockerfile
```

-	Layers:
	-	`sha256:dcdb3d8ac7a0180c710ff5f320266b3675307a76d43c648b83cd263d846d7f6d`  
		Last Modified: Wed, 24 Jul 2024 14:46:07 GMT  
		Size: 6.4 MB (6386381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17b9ccd98f4231b7162ab9a5e9eadb31d85ad4de3fe64de93570585a0b1c9622`  
		Last Modified: Wed, 24 Jul 2024 14:46:07 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c15ea28bde73880ab7f94027b9c05e2d4620a858958d672fd878ab8f5082364b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149176881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eee13f728fdf4dc2d94ef984aa65311be7fd3bf0d4f2441d60a1aa86bc9d41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2fd1362c98163030a52de79cafd3d14c1f56f0cbf2522eeab2c7845e36f421`  
		Last Modified: Tue, 13 Aug 2024 19:50:31 GMT  
		Size: 18.9 MB (18870195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90d8eb9c97f62b179fa41c54488c4a5099ad2be872c140f1e01b9e997ad71cf`  
		Last Modified: Tue, 13 Aug 2024 19:50:30 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30016fc60948562533654a15dd52496feada8d17a364f3fba24081990a51f93f`  
		Last Modified: Tue, 13 Aug 2024 19:51:05 GMT  
		Size: 57.1 MB (57123255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe90c4c1e966be3deeaf6987962b52e903fed2d1f08748d8372ccb3d9c1c2cdf`  
		Last Modified: Tue, 13 Aug 2024 19:51:03 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:10431b688df6bc8f1f01f64a4a6d1bdfd9ad1b4eb2203fce623956dba0f0921b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6406279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f6f99d2da727b90404a73202844b8ea710318690b3b9c8c04abee5f1f470d3`

```dockerfile
```

-	Layers:
	-	`sha256:0bd97d302fcee6750f95274d52513e2e7a30519eef63476d6c835b71c30cdec9`  
		Last Modified: Tue, 13 Aug 2024 19:51:04 GMT  
		Size: 6.4 MB (6391663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cef20fb611517b3a889bc0268cfbf4c86cab491e3913c7e9ded4bb88a22b709`  
		Last Modified: Tue, 13 Aug 2024 19:51:03 GMT  
		Size: 14.6 KB (14616 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.30.3-alpine`

```console
$ docker pull telegraf@sha256:97bb530cc385132152f0f171db0514dd3b852d6f1529f135de0d1c3ed4a64805
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.30.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:fcfe5222366ad62f02e065f1a69e45bce3bdc64e7cc6bcc20dd5f5ea12eb3977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68644019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242ce2c4f74738cd111a37d48992142573863a657f5421e6429e62662fe350da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc469e64f8855e42c6d4c6f121d649ce80b1b57b520030009bdb799aaf7b6d3`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd1dd2aea95e4d6aaeb5eadb1505da9fa8ba75ed038b99116d1289d3ee3607e`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 2.5 MB (2451682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da5b95773c156c402ef1eaaf6796f414895775753500372be983f0dc9d1d0ad`  
		Last Modified: Mon, 22 Jul 2024 23:04:34 GMT  
		Size: 62.6 MB (62568841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32432b32d0336088c3d13e71d5f2557b2fec10426fcfbd387f37801d9a94865b`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6e5a535211e37ba0525e30ae5b7005cffd5005998e7ce1cfaed15f200eeffd88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1070929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043244b274180f906f2a190fa8d7d09cbe1b5019f3de0040c8cfff6cf38cdc49`

```dockerfile
```

-	Layers:
	-	`sha256:47672bde33a0416036b3df7aa8668fc62f2d1b877370d59b5ca3a9e1118e1e0d`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 1.1 MB (1056195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3753d4298e51b5ffd45bfc070c77a5b4f56235122d929b090b405de0e4fd9aa`  
		Last Modified: Mon, 22 Jul 2024 23:04:33 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.30.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:75a9c7f73eedd98dc2b6a64d5e280a846580396dbf9beb921d86e186cd328313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63545852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e783d7f3d1a9a6923de67a97257eb420d2f5a3363f798f2c3bb1eedff90488`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.30.3
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da0d1ffb94d496286226e500ca461ae4c84a6368b8c23b64dfd72955579f654`  
		Last Modified: Wed, 24 Jul 2024 10:08:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c96666ef40bebea34c4984a3d34ddd3118468eb0087d117403688b0408735f6`  
		Last Modified: Wed, 24 Jul 2024 10:08:09 GMT  
		Size: 2.5 MB (2537424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e8a5942cbf5e0ef4d4255f119ce9d09d2c12a398538968aa5e78e2776d217a`  
		Last Modified: Wed, 24 Jul 2024 10:09:20 GMT  
		Size: 56.9 MB (56920887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474ac264b7008a9fabe6524487bd7bf820471fcb7bb5c600987ec44467b4d449`  
		Last Modified: Wed, 24 Jul 2024 10:09:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f9f7a61706ac67a335a92fa5448f8686290e0c1ce3689a186a08b620e16b3391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1066074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3486c7c0fa924d31507d7209b6055436fa9328a1f9bc101377f671ab00066071`

```dockerfile
```

-	Layers:
	-	`sha256:42bff7dffe23c1a81e044f9a8c3f5d35be7f93cba815e4da644691450f121e3a`  
		Last Modified: Wed, 24 Jul 2024 10:09:19 GMT  
		Size: 1.1 MB (1051065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d0280828ab5dc2c7606151e8005b003e9dd82e13f11311ad0775a53fc7161d`  
		Last Modified: Wed, 24 Jul 2024 10:09:18 GMT  
		Size: 15.0 KB (15009 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31`

```console
$ docker pull telegraf@sha256:95a3da18edd4c7541243b557df9caae7e0a61d911c40fcf072129e0de7c4fa44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31` - linux; amd64

```console
$ docker pull telegraf@sha256:b45de9809710167ccaab100b11e5956befe8ea50ef0f92babfba709233e74fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158840624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722fd31895d34d5c2963149b5b9dd9dc6c3b8074bc9853efac46d3972e98bf60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bac2f66285bd4f54507932dee524aa58dee6962eb872312d7207dd4fee8e324`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 18.9 MB (18947999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4823ef5cb4c32b89801eb0aa6a3925f175f8feea94aa5b30109fa1142dbadeba`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae870e415c652b38b6e6a8943103668c37ba1486d7ea20190dd42b9a8d471ab`  
		Last Modified: Tue, 13 Aug 2024 02:06:49 GMT  
		Size: 66.3 MB (66285438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6619767ff0a0354bb7dce4c0e71f1593be1f50f66b56a2e57f358a9d8c29db0`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:9ff13069a97d84bea834a00e135011bf8af9ac5f8c9e77d4f177ee1434cf3e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6414876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be40eab99ad60eada75b7247c2c93415ac32f2a5112263fcfc09f34c9748bc1b`

```dockerfile
```

-	Layers:
	-	`sha256:33086dd06cc352f5a93953623bb185510b3dd3ef88812beb274d1331acd123fc`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 6.4 MB (6400250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb0b6c9e23085aca7abc1b9da74ee83410cb8593f390b87b9e6af0ef927fd918`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 14.6 KB (14626 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:ce50a48f7439673ce482cc9bcdd276e8817d58a64093a707fe8edbc70894ed3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146502353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa10b0907063b7e50101aa2179b5b10290cdf511720ec9614a9f615d22cdcd25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4aab9bc50bc98996a3d0e7e05bf9fb7145601ae77302e2db1ab18aef96348e`  
		Last Modified: Mon, 12 Aug 2024 16:56:43 GMT  
		Size: 17.7 MB (17724865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4beddb4377fb3ec6fc74f20a67fbb100c90d3296fb77b6584a1ad5c565e1cf`  
		Last Modified: Mon, 12 Aug 2024 16:56:42 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0d21ea190d712ef07a7542e6f8ad9ff294795c333b47392e11a2111962c904`  
		Last Modified: Mon, 12 Aug 2024 16:56:44 GMT  
		Size: 61.7 MB (61672292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a8695db143b8b353ce624e768d8cca5ccf7c7ad7dd76a448497b4072533733`  
		Last Modified: Mon, 12 Aug 2024 16:56:42 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:262d9d5bb33389a87f469be8ce6732a6ca07f26e166c7ccb7c76f54d69020daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6410408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0448165e9793e64e6027b596b978858214249871638db0800a6a44976272a7b7`

```dockerfile
```

-	Layers:
	-	`sha256:3aafbf0f321244d9fad0211a58b87a39ec0fb6f0c4df4e9a2c2eb76c0f0879db`  
		Last Modified: Mon, 12 Aug 2024 16:56:42 GMT  
		Size: 6.4 MB (6395694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f76985fbeb34a012b6b5271cc7f7c9f924da5e60f64444a37eaa7c2a7f0018b`  
		Last Modified: Mon, 12 Aug 2024 16:56:42 GMT  
		Size: 14.7 KB (14714 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:7303af7d29d74d38605bfc94fd62d936ea8d42fed1515695e94d189a98c3537d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152431327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88fdbcff9e2b26c09fdf1ec2ef5845695d48b815047a770b3c0515b8a0cc9753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2fd1362c98163030a52de79cafd3d14c1f56f0cbf2522eeab2c7845e36f421`  
		Last Modified: Tue, 13 Aug 2024 19:50:31 GMT  
		Size: 18.9 MB (18870195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90d8eb9c97f62b179fa41c54488c4a5099ad2be872c140f1e01b9e997ad71cf`  
		Last Modified: Tue, 13 Aug 2024 19:50:30 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d924887578858e0e63937dcb06c02ea55c50acd4a86b57c08af049a2d548fb2`  
		Last Modified: Tue, 13 Aug 2024 19:51:42 GMT  
		Size: 60.4 MB (60377700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28788e21f4a2692acf6157bf03c3fa27ef8f6a6fc57922f510095a28fa80e0fa`  
		Last Modified: Tue, 13 Aug 2024 19:51:39 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:14a0be6cc37a23c99d9488415fa573f12dd555eb3a567a347fb4e89f6f91f819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6416708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb11f342a946e380637b3509e95bf887e9ee0028f9dc4e0e21f0f85a8ff6d302`

```dockerfile
```

-	Layers:
	-	`sha256:6258aab4d5ed7a15b2194a87571407f490d247b996708f9cf3f2246c5a8bc5af`  
		Last Modified: Tue, 13 Aug 2024 19:51:40 GMT  
		Size: 6.4 MB (6401777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d76a16deb22e84b6b9557fd9235d00d76c90da8e44489165d90c89422755b66f`  
		Last Modified: Tue, 13 Aug 2024 19:51:39 GMT  
		Size: 14.9 KB (14931 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31-alpine`

```console
$ docker pull telegraf@sha256:9f52c5e1ca21a0eae1d05d758904df4c8bc1aff7eca4f97f3134742347c45daa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:d5d40ac565ecd26025ac9dd3fab0b8b3805a30cb8a8081e63e181f1b5cbf5c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72153144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88347c5ad7332594511126fe4c31e0db9a6dbfe1788ee941a50201a690cef122`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d96f79ba57e9bfdec7d9011576873c104f3be71e5b9240a1a8a126194a5a353`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d395b78b6ead8e6044004820ae7bb2ff48550d479eb3e6484f3c4594e6fe2bde`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 2.5 MB (2451711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac422ca05692ac2502b016ef8bcbcba0cd65cd1bf87743c4baf08df4cbade1`  
		Last Modified: Mon, 12 Aug 2024 16:56:25 GMT  
		Size: 66.1 MB (66077933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc81c539d4116f636265e92a3b4330bc0b8b967253c0253c1f4bdfe209f089`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6946f808a772b2069f9759e6c35ca0e87c5750c21a1e242fba4c701381f18101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1079739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becd149d7b4943a02c3280c8f2d1884e4431aa94421e18c6b8f607f918bff33e`

```dockerfile
```

-	Layers:
	-	`sha256:71031225d67afa7f4e6359dc25d8e3462d1a3a88782584d662b461ffea0c62fb`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 1.1 MB (1064703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e152629635514b1bf072f80775060dafa431cbea6e70f7207d5e73a26b779eb8`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:945cf4c3e4f70222f67e1430fce86cf2e8759a8a0f57587953e8793bb9051a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66796515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905ac98277de19213d3346e8a85b6402c0ce8eaccd17a0a2c5aa779d211304bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1de5eaf2a1972853375a025a0309628552446763159c73f9fb971eedad7e97c`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a243aa4517b40d42c094f617342384531a20fde653e4378bdd44eec4445eeaa6`  
		Last Modified: Mon, 12 Aug 2024 17:49:47 GMT  
		Size: 2.5 MB (2537428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a3518efde0102230b00c4ee09fbc1dfdb976577cf2a7d5b83a69e7b43522bd`  
		Last Modified: Mon, 12 Aug 2024 17:49:48 GMT  
		Size: 60.2 MB (60171546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5484c079133258c45d9ec7d30cc2226199c8e5aa7696769a347a3cf4e8049c`  
		Last Modified: Mon, 12 Aug 2024 17:49:46 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4f5a831694c31de36d0073720172bc80c502074299db482033b7cdf7db62f56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1076501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb9eb546251758114a08c15fe33944dbfe034e7e3dc03d31e8933901a115dcb`

```dockerfile
```

-	Layers:
	-	`sha256:c292ce24841951032243ce2c3c4e54e5460412a18a74a5c87892e3a25132dcdb`  
		Last Modified: Mon, 12 Aug 2024 17:49:46 GMT  
		Size: 1.1 MB (1061177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ef0ee15b6c05bd92cdff902bfc9dca23eb9922078481588bb06a55df4031c15`  
		Last Modified: Mon, 12 Aug 2024 17:49:46 GMT  
		Size: 15.3 KB (15324 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3`

```console
$ docker pull telegraf@sha256:95a3da18edd4c7541243b557df9caae7e0a61d911c40fcf072129e0de7c4fa44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31.3` - linux; amd64

```console
$ docker pull telegraf@sha256:b45de9809710167ccaab100b11e5956befe8ea50ef0f92babfba709233e74fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158840624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722fd31895d34d5c2963149b5b9dd9dc6c3b8074bc9853efac46d3972e98bf60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bac2f66285bd4f54507932dee524aa58dee6962eb872312d7207dd4fee8e324`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 18.9 MB (18947999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4823ef5cb4c32b89801eb0aa6a3925f175f8feea94aa5b30109fa1142dbadeba`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae870e415c652b38b6e6a8943103668c37ba1486d7ea20190dd42b9a8d471ab`  
		Last Modified: Tue, 13 Aug 2024 02:06:49 GMT  
		Size: 66.3 MB (66285438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6619767ff0a0354bb7dce4c0e71f1593be1f50f66b56a2e57f358a9d8c29db0`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:9ff13069a97d84bea834a00e135011bf8af9ac5f8c9e77d4f177ee1434cf3e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6414876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be40eab99ad60eada75b7247c2c93415ac32f2a5112263fcfc09f34c9748bc1b`

```dockerfile
```

-	Layers:
	-	`sha256:33086dd06cc352f5a93953623bb185510b3dd3ef88812beb274d1331acd123fc`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 6.4 MB (6400250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb0b6c9e23085aca7abc1b9da74ee83410cb8593f390b87b9e6af0ef927fd918`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 14.6 KB (14626 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:ce50a48f7439673ce482cc9bcdd276e8817d58a64093a707fe8edbc70894ed3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146502353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa10b0907063b7e50101aa2179b5b10290cdf511720ec9614a9f615d22cdcd25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4aab9bc50bc98996a3d0e7e05bf9fb7145601ae77302e2db1ab18aef96348e`  
		Last Modified: Mon, 12 Aug 2024 16:56:43 GMT  
		Size: 17.7 MB (17724865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4beddb4377fb3ec6fc74f20a67fbb100c90d3296fb77b6584a1ad5c565e1cf`  
		Last Modified: Mon, 12 Aug 2024 16:56:42 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0d21ea190d712ef07a7542e6f8ad9ff294795c333b47392e11a2111962c904`  
		Last Modified: Mon, 12 Aug 2024 16:56:44 GMT  
		Size: 61.7 MB (61672292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a8695db143b8b353ce624e768d8cca5ccf7c7ad7dd76a448497b4072533733`  
		Last Modified: Mon, 12 Aug 2024 16:56:42 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:262d9d5bb33389a87f469be8ce6732a6ca07f26e166c7ccb7c76f54d69020daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6410408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0448165e9793e64e6027b596b978858214249871638db0800a6a44976272a7b7`

```dockerfile
```

-	Layers:
	-	`sha256:3aafbf0f321244d9fad0211a58b87a39ec0fb6f0c4df4e9a2c2eb76c0f0879db`  
		Last Modified: Mon, 12 Aug 2024 16:56:42 GMT  
		Size: 6.4 MB (6395694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f76985fbeb34a012b6b5271cc7f7c9f924da5e60f64444a37eaa7c2a7f0018b`  
		Last Modified: Mon, 12 Aug 2024 16:56:42 GMT  
		Size: 14.7 KB (14714 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:7303af7d29d74d38605bfc94fd62d936ea8d42fed1515695e94d189a98c3537d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152431327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88fdbcff9e2b26c09fdf1ec2ef5845695d48b815047a770b3c0515b8a0cc9753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2fd1362c98163030a52de79cafd3d14c1f56f0cbf2522eeab2c7845e36f421`  
		Last Modified: Tue, 13 Aug 2024 19:50:31 GMT  
		Size: 18.9 MB (18870195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90d8eb9c97f62b179fa41c54488c4a5099ad2be872c140f1e01b9e997ad71cf`  
		Last Modified: Tue, 13 Aug 2024 19:50:30 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d924887578858e0e63937dcb06c02ea55c50acd4a86b57c08af049a2d548fb2`  
		Last Modified: Tue, 13 Aug 2024 19:51:42 GMT  
		Size: 60.4 MB (60377700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28788e21f4a2692acf6157bf03c3fa27ef8f6a6fc57922f510095a28fa80e0fa`  
		Last Modified: Tue, 13 Aug 2024 19:51:39 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:14a0be6cc37a23c99d9488415fa573f12dd555eb3a567a347fb4e89f6f91f819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6416708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb11f342a946e380637b3509e95bf887e9ee0028f9dc4e0e21f0f85a8ff6d302`

```dockerfile
```

-	Layers:
	-	`sha256:6258aab4d5ed7a15b2194a87571407f490d247b996708f9cf3f2246c5a8bc5af`  
		Last Modified: Tue, 13 Aug 2024 19:51:40 GMT  
		Size: 6.4 MB (6401777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d76a16deb22e84b6b9557fd9235d00d76c90da8e44489165d90c89422755b66f`  
		Last Modified: Tue, 13 Aug 2024 19:51:39 GMT  
		Size: 14.9 KB (14931 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3-alpine`

```console
$ docker pull telegraf@sha256:9f52c5e1ca21a0eae1d05d758904df4c8bc1aff7eca4f97f3134742347c45daa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:d5d40ac565ecd26025ac9dd3fab0b8b3805a30cb8a8081e63e181f1b5cbf5c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72153144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88347c5ad7332594511126fe4c31e0db9a6dbfe1788ee941a50201a690cef122`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d96f79ba57e9bfdec7d9011576873c104f3be71e5b9240a1a8a126194a5a353`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d395b78b6ead8e6044004820ae7bb2ff48550d479eb3e6484f3c4594e6fe2bde`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 2.5 MB (2451711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac422ca05692ac2502b016ef8bcbcba0cd65cd1bf87743c4baf08df4cbade1`  
		Last Modified: Mon, 12 Aug 2024 16:56:25 GMT  
		Size: 66.1 MB (66077933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc81c539d4116f636265e92a3b4330bc0b8b967253c0253c1f4bdfe209f089`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6946f808a772b2069f9759e6c35ca0e87c5750c21a1e242fba4c701381f18101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1079739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becd149d7b4943a02c3280c8f2d1884e4431aa94421e18c6b8f607f918bff33e`

```dockerfile
```

-	Layers:
	-	`sha256:71031225d67afa7f4e6359dc25d8e3462d1a3a88782584d662b461ffea0c62fb`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 1.1 MB (1064703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e152629635514b1bf072f80775060dafa431cbea6e70f7207d5e73a26b779eb8`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:945cf4c3e4f70222f67e1430fce86cf2e8759a8a0f57587953e8793bb9051a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66796515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905ac98277de19213d3346e8a85b6402c0ce8eaccd17a0a2c5aa779d211304bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1de5eaf2a1972853375a025a0309628552446763159c73f9fb971eedad7e97c`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a243aa4517b40d42c094f617342384531a20fde653e4378bdd44eec4445eeaa6`  
		Last Modified: Mon, 12 Aug 2024 17:49:47 GMT  
		Size: 2.5 MB (2537428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a3518efde0102230b00c4ee09fbc1dfdb976577cf2a7d5b83a69e7b43522bd`  
		Last Modified: Mon, 12 Aug 2024 17:49:48 GMT  
		Size: 60.2 MB (60171546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5484c079133258c45d9ec7d30cc2226199c8e5aa7696769a347a3cf4e8049c`  
		Last Modified: Mon, 12 Aug 2024 17:49:46 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4f5a831694c31de36d0073720172bc80c502074299db482033b7cdf7db62f56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1076501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb9eb546251758114a08c15fe33944dbfe034e7e3dc03d31e8933901a115dcb`

```dockerfile
```

-	Layers:
	-	`sha256:c292ce24841951032243ce2c3c4e54e5460412a18a74a5c87892e3a25132dcdb`  
		Last Modified: Mon, 12 Aug 2024 17:49:46 GMT  
		Size: 1.1 MB (1061177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ef0ee15b6c05bd92cdff902bfc9dca23eb9922078481588bb06a55df4031c15`  
		Last Modified: Mon, 12 Aug 2024 17:49:46 GMT  
		Size: 15.3 KB (15324 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:9f52c5e1ca21a0eae1d05d758904df4c8bc1aff7eca4f97f3134742347c45daa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:d5d40ac565ecd26025ac9dd3fab0b8b3805a30cb8a8081e63e181f1b5cbf5c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72153144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88347c5ad7332594511126fe4c31e0db9a6dbfe1788ee941a50201a690cef122`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d96f79ba57e9bfdec7d9011576873c104f3be71e5b9240a1a8a126194a5a353`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d395b78b6ead8e6044004820ae7bb2ff48550d479eb3e6484f3c4594e6fe2bde`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 2.5 MB (2451711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac422ca05692ac2502b016ef8bcbcba0cd65cd1bf87743c4baf08df4cbade1`  
		Last Modified: Mon, 12 Aug 2024 16:56:25 GMT  
		Size: 66.1 MB (66077933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc81c539d4116f636265e92a3b4330bc0b8b967253c0253c1f4bdfe209f089`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6946f808a772b2069f9759e6c35ca0e87c5750c21a1e242fba4c701381f18101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1079739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becd149d7b4943a02c3280c8f2d1884e4431aa94421e18c6b8f607f918bff33e`

```dockerfile
```

-	Layers:
	-	`sha256:71031225d67afa7f4e6359dc25d8e3462d1a3a88782584d662b461ffea0c62fb`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 1.1 MB (1064703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e152629635514b1bf072f80775060dafa431cbea6e70f7207d5e73a26b779eb8`  
		Last Modified: Mon, 12 Aug 2024 16:56:23 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:945cf4c3e4f70222f67e1430fce86cf2e8759a8a0f57587953e8793bb9051a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66796515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905ac98277de19213d3346e8a85b6402c0ce8eaccd17a0a2c5aa779d211304bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1de5eaf2a1972853375a025a0309628552446763159c73f9fb971eedad7e97c`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a243aa4517b40d42c094f617342384531a20fde653e4378bdd44eec4445eeaa6`  
		Last Modified: Mon, 12 Aug 2024 17:49:47 GMT  
		Size: 2.5 MB (2537428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a3518efde0102230b00c4ee09fbc1dfdb976577cf2a7d5b83a69e7b43522bd`  
		Last Modified: Mon, 12 Aug 2024 17:49:48 GMT  
		Size: 60.2 MB (60171546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5484c079133258c45d9ec7d30cc2226199c8e5aa7696769a347a3cf4e8049c`  
		Last Modified: Mon, 12 Aug 2024 17:49:46 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4f5a831694c31de36d0073720172bc80c502074299db482033b7cdf7db62f56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1076501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb9eb546251758114a08c15fe33944dbfe034e7e3dc03d31e8933901a115dcb`

```dockerfile
```

-	Layers:
	-	`sha256:c292ce24841951032243ce2c3c4e54e5460412a18a74a5c87892e3a25132dcdb`  
		Last Modified: Mon, 12 Aug 2024 17:49:46 GMT  
		Size: 1.1 MB (1061177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ef0ee15b6c05bd92cdff902bfc9dca23eb9922078481588bb06a55df4031c15`  
		Last Modified: Mon, 12 Aug 2024 17:49:46 GMT  
		Size: 15.3 KB (15324 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:95a3da18edd4c7541243b557df9caae7e0a61d911c40fcf072129e0de7c4fa44
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
$ docker pull telegraf@sha256:b45de9809710167ccaab100b11e5956befe8ea50ef0f92babfba709233e74fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158840624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722fd31895d34d5c2963149b5b9dd9dc6c3b8074bc9853efac46d3972e98bf60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bac2f66285bd4f54507932dee524aa58dee6962eb872312d7207dd4fee8e324`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 18.9 MB (18947999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4823ef5cb4c32b89801eb0aa6a3925f175f8feea94aa5b30109fa1142dbadeba`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae870e415c652b38b6e6a8943103668c37ba1486d7ea20190dd42b9a8d471ab`  
		Last Modified: Tue, 13 Aug 2024 02:06:49 GMT  
		Size: 66.3 MB (66285438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6619767ff0a0354bb7dce4c0e71f1593be1f50f66b56a2e57f358a9d8c29db0`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:9ff13069a97d84bea834a00e135011bf8af9ac5f8c9e77d4f177ee1434cf3e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6414876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be40eab99ad60eada75b7247c2c93415ac32f2a5112263fcfc09f34c9748bc1b`

```dockerfile
```

-	Layers:
	-	`sha256:33086dd06cc352f5a93953623bb185510b3dd3ef88812beb274d1331acd123fc`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 6.4 MB (6400250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb0b6c9e23085aca7abc1b9da74ee83410cb8593f390b87b9e6af0ef927fd918`  
		Last Modified: Tue, 13 Aug 2024 02:06:48 GMT  
		Size: 14.6 KB (14626 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:ce50a48f7439673ce482cc9bcdd276e8817d58a64093a707fe8edbc70894ed3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146502353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa10b0907063b7e50101aa2179b5b10290cdf511720ec9614a9f615d22cdcd25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4aab9bc50bc98996a3d0e7e05bf9fb7145601ae77302e2db1ab18aef96348e`  
		Last Modified: Mon, 12 Aug 2024 16:56:43 GMT  
		Size: 17.7 MB (17724865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4beddb4377fb3ec6fc74f20a67fbb100c90d3296fb77b6584a1ad5c565e1cf`  
		Last Modified: Mon, 12 Aug 2024 16:56:42 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0d21ea190d712ef07a7542e6f8ad9ff294795c333b47392e11a2111962c904`  
		Last Modified: Mon, 12 Aug 2024 16:56:44 GMT  
		Size: 61.7 MB (61672292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a8695db143b8b353ce624e768d8cca5ccf7c7ad7dd76a448497b4072533733`  
		Last Modified: Mon, 12 Aug 2024 16:56:42 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:262d9d5bb33389a87f469be8ce6732a6ca07f26e166c7ccb7c76f54d69020daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6410408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0448165e9793e64e6027b596b978858214249871638db0800a6a44976272a7b7`

```dockerfile
```

-	Layers:
	-	`sha256:3aafbf0f321244d9fad0211a58b87a39ec0fb6f0c4df4e9a2c2eb76c0f0879db`  
		Last Modified: Mon, 12 Aug 2024 16:56:42 GMT  
		Size: 6.4 MB (6395694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f76985fbeb34a012b6b5271cc7f7c9f924da5e60f64444a37eaa7c2a7f0018b`  
		Last Modified: Mon, 12 Aug 2024 16:56:42 GMT  
		Size: 14.7 KB (14714 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:7303af7d29d74d38605bfc94fd62d936ea8d42fed1515695e94d189a98c3537d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152431327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88fdbcff9e2b26c09fdf1ec2ef5845695d48b815047a770b3c0515b8a0cc9753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 12 Aug 2024 15:27:35 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Aug 2024 15:27:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 12 Aug 2024 15:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 12 Aug 2024 15:27:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 12 Aug 2024 15:27:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 15:27:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2fd1362c98163030a52de79cafd3d14c1f56f0cbf2522eeab2c7845e36f421`  
		Last Modified: Tue, 13 Aug 2024 19:50:31 GMT  
		Size: 18.9 MB (18870195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90d8eb9c97f62b179fa41c54488c4a5099ad2be872c140f1e01b9e997ad71cf`  
		Last Modified: Tue, 13 Aug 2024 19:50:30 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d924887578858e0e63937dcb06c02ea55c50acd4a86b57c08af049a2d548fb2`  
		Last Modified: Tue, 13 Aug 2024 19:51:42 GMT  
		Size: 60.4 MB (60377700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28788e21f4a2692acf6157bf03c3fa27ef8f6a6fc57922f510095a28fa80e0fa`  
		Last Modified: Tue, 13 Aug 2024 19:51:39 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:14a0be6cc37a23c99d9488415fa573f12dd555eb3a567a347fb4e89f6f91f819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6416708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb11f342a946e380637b3509e95bf887e9ee0028f9dc4e0e21f0f85a8ff6d302`

```dockerfile
```

-	Layers:
	-	`sha256:6258aab4d5ed7a15b2194a87571407f490d247b996708f9cf3f2246c5a8bc5af`  
		Last Modified: Tue, 13 Aug 2024 19:51:40 GMT  
		Size: 6.4 MB (6401777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d76a16deb22e84b6b9557fd9235d00d76c90da8e44489165d90c89422755b66f`  
		Last Modified: Tue, 13 Aug 2024 19:51:39 GMT  
		Size: 14.9 KB (14931 bytes)  
		MIME: application/vnd.in-toto+json
