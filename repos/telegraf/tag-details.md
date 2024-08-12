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
$ docker pull telegraf@sha256:d0162bdad8a758c3a87073237a4437ad3ddc835e47e60c1baa3b573540ec6c51
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
$ docker pull telegraf@sha256:73eb27350b6a7521877823792b306df3cb8043d3d592b5216e21a640f2b2ec55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155197811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68bb8e071ebb7aa29a8786f1076f72c63282e3ca99474f9aee2fafb5455d6136`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
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
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6391e7d69d53f0456deba2a83a792af047bc1da9b6f6426a8e5ee175d8c4ed`  
		Last Modified: Tue, 23 Jul 2024 07:28:25 GMT  
		Size: 18.9 MB (18948050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1244d3237cfe4c9a01725351e5a854ccfc084e2d17473135abb7435a41a0f123`  
		Last Modified: Tue, 23 Jul 2024 07:28:25 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cae12cd61a35f90a02140cf3d8b6f8c85ddce332060b0de56ad58ddd2cea1b`  
		Last Modified: Tue, 23 Jul 2024 07:28:26 GMT  
		Size: 62.6 MB (62642480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46daeb4df0ccdb428c3e503451823bc3b2bc8c7e2be3ab3f577db93589631f87`  
		Last Modified: Tue, 23 Jul 2024 07:28:25 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:5d65375ae04adc0b5e1723a0e81f03a29589ee7981b6a5da5e92acd338036f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdf50fa8834da5fd89d9dd56a20a3f404202fba5a0596929f6728a0c6f9795f`

```dockerfile
```

-	Layers:
	-	`sha256:214b9ee0e4300c2803da44eb2196e67e44098305f3dabb66116183455a32c949`  
		Last Modified: Tue, 23 Jul 2024 07:28:25 GMT  
		Size: 6.4 MB (6391319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1731121707aa161703f652cd0ce52ea1a0746cac833ad78502c4590b6938c7a2`  
		Last Modified: Tue, 23 Jul 2024 07:28:25 GMT  
		Size: 14.3 KB (14324 bytes)  
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
$ docker pull telegraf@sha256:3bebdd48b800149985e8c7f4f5d59b0fccc1f195998d9fbf990e94cbc8fe0a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149035012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ea0c40bc5a1dc69a02f0eb8dc8b1d123e6a570dce609c25dcb4661ec789be3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b062d54ff26a5353c5c0b8c6f810469d5ef2e6f0303052c6d29c088fb88a5b85`  
		Last Modified: Wed, 24 Jul 2024 10:07:35 GMT  
		Size: 18.9 MB (18870600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2b47224b7f91d883d4bab981357b11f6ddd8b305a34dee2cb3e85b1421d80d`  
		Last Modified: Wed, 24 Jul 2024 10:07:34 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48cb0cd7039f9b0a2098758587b818feed7ff2fcc94ba942723581816728fb9`  
		Last Modified: Wed, 24 Jul 2024 10:07:36 GMT  
		Size: 57.0 MB (56981110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ffcd574f0dbdcdbac060a0245d578e2b6b76923ca1509af2604b4ac553b3db`  
		Last Modified: Wed, 24 Jul 2024 10:07:34 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29` - unknown; unknown

```console
$ docker pull telegraf@sha256:021720108934df5c972d31b604c51cc8917d3aa54d3e31c1a3258b175bed731e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ddb4c66a03051298232384d3eecd40820d643bba62b3e23dbefb0cf6200914c`

```dockerfile
```

-	Layers:
	-	`sha256:cab0d618dd465c1ece878a32dc345b01afa430bfe695d61984d0ac3a0513985a`  
		Last Modified: Wed, 24 Jul 2024 10:07:35 GMT  
		Size: 6.4 MB (6391242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7994a5d69560c87060114a3ae949b62b4c36f3f07f75fb8f8a6a307c79217803`  
		Last Modified: Wed, 24 Jul 2024 10:07:34 GMT  
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
$ docker pull telegraf@sha256:d0162bdad8a758c3a87073237a4437ad3ddc835e47e60c1baa3b573540ec6c51
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
$ docker pull telegraf@sha256:73eb27350b6a7521877823792b306df3cb8043d3d592b5216e21a640f2b2ec55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155197811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68bb8e071ebb7aa29a8786f1076f72c63282e3ca99474f9aee2fafb5455d6136`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
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
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6391e7d69d53f0456deba2a83a792af047bc1da9b6f6426a8e5ee175d8c4ed`  
		Last Modified: Tue, 23 Jul 2024 07:28:25 GMT  
		Size: 18.9 MB (18948050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1244d3237cfe4c9a01725351e5a854ccfc084e2d17473135abb7435a41a0f123`  
		Last Modified: Tue, 23 Jul 2024 07:28:25 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cae12cd61a35f90a02140cf3d8b6f8c85ddce332060b0de56ad58ddd2cea1b`  
		Last Modified: Tue, 23 Jul 2024 07:28:26 GMT  
		Size: 62.6 MB (62642480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46daeb4df0ccdb428c3e503451823bc3b2bc8c7e2be3ab3f577db93589631f87`  
		Last Modified: Tue, 23 Jul 2024 07:28:25 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:5d65375ae04adc0b5e1723a0e81f03a29589ee7981b6a5da5e92acd338036f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdf50fa8834da5fd89d9dd56a20a3f404202fba5a0596929f6728a0c6f9795f`

```dockerfile
```

-	Layers:
	-	`sha256:214b9ee0e4300c2803da44eb2196e67e44098305f3dabb66116183455a32c949`  
		Last Modified: Tue, 23 Jul 2024 07:28:25 GMT  
		Size: 6.4 MB (6391319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1731121707aa161703f652cd0ce52ea1a0746cac833ad78502c4590b6938c7a2`  
		Last Modified: Tue, 23 Jul 2024 07:28:25 GMT  
		Size: 14.3 KB (14324 bytes)  
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
$ docker pull telegraf@sha256:3bebdd48b800149985e8c7f4f5d59b0fccc1f195998d9fbf990e94cbc8fe0a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149035012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ea0c40bc5a1dc69a02f0eb8dc8b1d123e6a570dce609c25dcb4661ec789be3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b062d54ff26a5353c5c0b8c6f810469d5ef2e6f0303052c6d29c088fb88a5b85`  
		Last Modified: Wed, 24 Jul 2024 10:07:35 GMT  
		Size: 18.9 MB (18870600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2b47224b7f91d883d4bab981357b11f6ddd8b305a34dee2cb3e85b1421d80d`  
		Last Modified: Wed, 24 Jul 2024 10:07:34 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48cb0cd7039f9b0a2098758587b818feed7ff2fcc94ba942723581816728fb9`  
		Last Modified: Wed, 24 Jul 2024 10:07:36 GMT  
		Size: 57.0 MB (56981110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ffcd574f0dbdcdbac060a0245d578e2b6b76923ca1509af2604b4ac553b3db`  
		Last Modified: Wed, 24 Jul 2024 10:07:34 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.29.5` - unknown; unknown

```console
$ docker pull telegraf@sha256:021720108934df5c972d31b604c51cc8917d3aa54d3e31c1a3258b175bed731e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6405859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ddb4c66a03051298232384d3eecd40820d643bba62b3e23dbefb0cf6200914c`

```dockerfile
```

-	Layers:
	-	`sha256:cab0d618dd465c1ece878a32dc345b01afa430bfe695d61984d0ac3a0513985a`  
		Last Modified: Wed, 24 Jul 2024 10:07:35 GMT  
		Size: 6.4 MB (6391242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7994a5d69560c87060114a3ae949b62b4c36f3f07f75fb8f8a6a307c79217803`  
		Last Modified: Wed, 24 Jul 2024 10:07:34 GMT  
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
$ docker pull telegraf@sha256:41d592afa2babb2ac058f3b925670f94c56daeea909db8cc81a2214077e6ae35
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
$ docker pull telegraf@sha256:53c5a6d5a2142544139877b1a0d54c5f310a14efd1cbf5f09a64c975459c7c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155321768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3b1dd875d8ac0ceff2cb59a48e61152095d5bd332113d97a138aa98890bdc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
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
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82581daee33eeb3be39bfbbb7f004a528459c011077f09fb223c0aec83ba6909`  
		Last Modified: Tue, 23 Jul 2024 07:28:24 GMT  
		Size: 18.9 MB (18948047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e58f28c3ab51a0cbfb4ce2cbd6393b274dd2b51089fd90c27afd0fb2219473`  
		Last Modified: Tue, 23 Jul 2024 07:28:24 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d843587b199a153acdb79cca9885c447897c4e7bfc1e52aff53cdee1ea8adede`  
		Last Modified: Tue, 23 Jul 2024 07:28:25 GMT  
		Size: 62.8 MB (62766453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd1f4c117c45c7c44f50890a9db357ec12763a08814a5be52c71d5356c26dea`  
		Last Modified: Tue, 23 Jul 2024 07:28:24 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:c5ffff85e818efa5bb1f06b613001947d932476981ef7e6bae0bfbd3b4daa28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6406066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67944b3cd62dde5e64a3b417d0afd4d845a18284de611b18bb7e5ad599920d0`

```dockerfile
```

-	Layers:
	-	`sha256:c4df91531976f6c3767ae25676b905bd4a63d5fc80cb3f0cbf32f57360c236e4`  
		Last Modified: Tue, 23 Jul 2024 07:28:24 GMT  
		Size: 6.4 MB (6391742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31c7267ad570951f4d3edc0c798d67041bc518f95a88576b3b303f194b7a5e71`  
		Last Modified: Tue, 23 Jul 2024 07:28:24 GMT  
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
$ docker pull telegraf@sha256:bac5a3766c361cc4f15a40607adc465c567c551c6b3ac1c2e689d839e73399cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149177124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd42c5c8cd2802023d31ed3605496116458bce55bbf50f6fd9ccd12c47f03de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b062d54ff26a5353c5c0b8c6f810469d5ef2e6f0303052c6d29c088fb88a5b85`  
		Last Modified: Wed, 24 Jul 2024 10:07:35 GMT  
		Size: 18.9 MB (18870600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2b47224b7f91d883d4bab981357b11f6ddd8b305a34dee2cb3e85b1421d80d`  
		Last Modified: Wed, 24 Jul 2024 10:07:34 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73aeabb81ee7c1f1ea45ec298d4509bea4e20069833e9e1df15c93135b9fef9`  
		Last Modified: Wed, 24 Jul 2024 10:08:47 GMT  
		Size: 57.1 MB (57123224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7668886eedc4b65a6d03cb5af9586996e47bb9403a37c0e25d0619bbb65eee6`  
		Last Modified: Wed, 24 Jul 2024 10:08:45 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30` - unknown; unknown

```console
$ docker pull telegraf@sha256:c603424628779d40ca4bbbd5132f9a98294b0efa09ad04c846a9ffd14008d3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6406281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae9ddd829fad9764fb2cb03fb50f3385b5e4510b247dba1ade80812650641b0`

```dockerfile
```

-	Layers:
	-	`sha256:a33d9cdeaacd30eff05340c4e22e38865d265ee271184f076c927423287c8181`  
		Last Modified: Wed, 24 Jul 2024 10:08:46 GMT  
		Size: 6.4 MB (6391665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16b99cea642849c58d688488e9e58a0f10fbce85aa276cd3f0ec55a0828e5b41`  
		Last Modified: Wed, 24 Jul 2024 10:08:45 GMT  
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
$ docker pull telegraf@sha256:41d592afa2babb2ac058f3b925670f94c56daeea909db8cc81a2214077e6ae35
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
$ docker pull telegraf@sha256:53c5a6d5a2142544139877b1a0d54c5f310a14efd1cbf5f09a64c975459c7c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155321768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3b1dd875d8ac0ceff2cb59a48e61152095d5bd332113d97a138aa98890bdc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
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
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82581daee33eeb3be39bfbbb7f004a528459c011077f09fb223c0aec83ba6909`  
		Last Modified: Tue, 23 Jul 2024 07:28:24 GMT  
		Size: 18.9 MB (18948047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e58f28c3ab51a0cbfb4ce2cbd6393b274dd2b51089fd90c27afd0fb2219473`  
		Last Modified: Tue, 23 Jul 2024 07:28:24 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d843587b199a153acdb79cca9885c447897c4e7bfc1e52aff53cdee1ea8adede`  
		Last Modified: Tue, 23 Jul 2024 07:28:25 GMT  
		Size: 62.8 MB (62766453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd1f4c117c45c7c44f50890a9db357ec12763a08814a5be52c71d5356c26dea`  
		Last Modified: Tue, 23 Jul 2024 07:28:24 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:c5ffff85e818efa5bb1f06b613001947d932476981ef7e6bae0bfbd3b4daa28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6406066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67944b3cd62dde5e64a3b417d0afd4d845a18284de611b18bb7e5ad599920d0`

```dockerfile
```

-	Layers:
	-	`sha256:c4df91531976f6c3767ae25676b905bd4a63d5fc80cb3f0cbf32f57360c236e4`  
		Last Modified: Tue, 23 Jul 2024 07:28:24 GMT  
		Size: 6.4 MB (6391742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31c7267ad570951f4d3edc0c798d67041bc518f95a88576b3b303f194b7a5e71`  
		Last Modified: Tue, 23 Jul 2024 07:28:24 GMT  
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
$ docker pull telegraf@sha256:bac5a3766c361cc4f15a40607adc465c567c551c6b3ac1c2e689d839e73399cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149177124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd42c5c8cd2802023d31ed3605496116458bce55bbf50f6fd9ccd12c47f03de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b062d54ff26a5353c5c0b8c6f810469d5ef2e6f0303052c6d29c088fb88a5b85`  
		Last Modified: Wed, 24 Jul 2024 10:07:35 GMT  
		Size: 18.9 MB (18870600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2b47224b7f91d883d4bab981357b11f6ddd8b305a34dee2cb3e85b1421d80d`  
		Last Modified: Wed, 24 Jul 2024 10:07:34 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73aeabb81ee7c1f1ea45ec298d4509bea4e20069833e9e1df15c93135b9fef9`  
		Last Modified: Wed, 24 Jul 2024 10:08:47 GMT  
		Size: 57.1 MB (57123224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7668886eedc4b65a6d03cb5af9586996e47bb9403a37c0e25d0619bbb65eee6`  
		Last Modified: Wed, 24 Jul 2024 10:08:45 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.30.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:c603424628779d40ca4bbbd5132f9a98294b0efa09ad04c846a9ffd14008d3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6406281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae9ddd829fad9764fb2cb03fb50f3385b5e4510b247dba1ade80812650641b0`

```dockerfile
```

-	Layers:
	-	`sha256:a33d9cdeaacd30eff05340c4e22e38865d265ee271184f076c927423287c8181`  
		Last Modified: Wed, 24 Jul 2024 10:08:46 GMT  
		Size: 6.4 MB (6391665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16b99cea642849c58d688488e9e58a0f10fbce85aa276cd3f0ec55a0828e5b41`  
		Last Modified: Wed, 24 Jul 2024 10:08:45 GMT  
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
$ docker pull telegraf@sha256:5c87b2f498fa551ab0164c07777e1df21512153e3535eaab4f22164ad0896ea0
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
$ docker pull telegraf@sha256:db955b6f6e5d697a24fe1655ac0c20296527ac44a23436dd00fa39706be5b4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158840614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47dcb17e463f64c992c23fd642e9e2c2259d5e155a9cbde08fb6c151687831e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
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
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef53abc2411c102594507d05da0326efee54a35ea0a832399a3c231758cbaab`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 18.9 MB (18947939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef54e99c1fb93cf2e64602736f7d62bfaa826b6093aaa0543a3714e0f9449dc1`  
		Last Modified: Mon, 12 Aug 2024 16:56:29 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5ea27e8eabae411b9ec797800b59be391907fa47e3c9127354a8a4a133550a`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 66.3 MB (66285397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa599aa3e0f8f0e5b862286162323f1bf0554925852872f0125cdb86cde61d8`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:b6f24294f61ff2befcdb2a80bfd9344aae285e9aec81b1aaee914da6200aab2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6414876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2071c80837710be49f8d8b7f93122f10940b10131bf56e29323d3ea7ad63b28f`

```dockerfile
```

-	Layers:
	-	`sha256:c9b840baaccc3dec7c803b551cdd913200ebc48b18ef60be1cdc7e2d2aeab75c`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 6.4 MB (6400250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98dd4b3983ef5a196027bd2fc2ee9798c9fe98534ddc285ab4915ebd588fd82b`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
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
$ docker pull telegraf@sha256:36f588bdc36bcec7c4043ceed4c930969c7ecd1e930d1a86a89c657d7f1383ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152431766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539353e4a9fad92c41520adea75209798022d6a681535e7fdc91dce0f6bfa71b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:03:32 GMT
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b7ed4c60331ced332bcb048e97f71fd70743fa6ddf845d25299fbd066f9e37`  
		Last Modified: Mon, 12 Aug 2024 17:49:10 GMT  
		Size: 18.9 MB (18870715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9ece39bd7a0cbb5d239333d404288aab076519704cf6335ef02807d84d25ae`  
		Last Modified: Mon, 12 Aug 2024 17:49:09 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05d6fb7e6e26fa86b8e3b3f771c089546b401dff70d11b35f39c9345f0a079e`  
		Last Modified: Mon, 12 Aug 2024 17:49:12 GMT  
		Size: 60.4 MB (60377758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a84c185b1825709c97051ae98d431ec05d246c2e35c62b32437bf7f15b8489a`  
		Last Modified: Mon, 12 Aug 2024 17:49:10 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:00239ba7660092681bf1ade0ab0e762b6c905f26d8a9d022e73e55e1392bb7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6416708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6533b26091b04fb85d134b608388e0ae62cd36c1c07c41f98b74f4ba99383b`

```dockerfile
```

-	Layers:
	-	`sha256:4ca2c3b9aa62271698d1be5b387f653b15258ec26a042987d5225f1e7d3f2015`  
		Last Modified: Mon, 12 Aug 2024 17:49:10 GMT  
		Size: 6.4 MB (6401777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9828de6fad1b6dac72395f2e472690cbd2d9f22e8def908cdde91c080a55ad`  
		Last Modified: Mon, 12 Aug 2024 17:49:10 GMT  
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
$ docker pull telegraf@sha256:5c87b2f498fa551ab0164c07777e1df21512153e3535eaab4f22164ad0896ea0
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
$ docker pull telegraf@sha256:db955b6f6e5d697a24fe1655ac0c20296527ac44a23436dd00fa39706be5b4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158840614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47dcb17e463f64c992c23fd642e9e2c2259d5e155a9cbde08fb6c151687831e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
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
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef53abc2411c102594507d05da0326efee54a35ea0a832399a3c231758cbaab`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 18.9 MB (18947939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef54e99c1fb93cf2e64602736f7d62bfaa826b6093aaa0543a3714e0f9449dc1`  
		Last Modified: Mon, 12 Aug 2024 16:56:29 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5ea27e8eabae411b9ec797800b59be391907fa47e3c9127354a8a4a133550a`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 66.3 MB (66285397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa599aa3e0f8f0e5b862286162323f1bf0554925852872f0125cdb86cde61d8`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:b6f24294f61ff2befcdb2a80bfd9344aae285e9aec81b1aaee914da6200aab2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6414876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2071c80837710be49f8d8b7f93122f10940b10131bf56e29323d3ea7ad63b28f`

```dockerfile
```

-	Layers:
	-	`sha256:c9b840baaccc3dec7c803b551cdd913200ebc48b18ef60be1cdc7e2d2aeab75c`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 6.4 MB (6400250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98dd4b3983ef5a196027bd2fc2ee9798c9fe98534ddc285ab4915ebd588fd82b`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
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
$ docker pull telegraf@sha256:36f588bdc36bcec7c4043ceed4c930969c7ecd1e930d1a86a89c657d7f1383ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152431766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539353e4a9fad92c41520adea75209798022d6a681535e7fdc91dce0f6bfa71b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:03:32 GMT
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b7ed4c60331ced332bcb048e97f71fd70743fa6ddf845d25299fbd066f9e37`  
		Last Modified: Mon, 12 Aug 2024 17:49:10 GMT  
		Size: 18.9 MB (18870715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9ece39bd7a0cbb5d239333d404288aab076519704cf6335ef02807d84d25ae`  
		Last Modified: Mon, 12 Aug 2024 17:49:09 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05d6fb7e6e26fa86b8e3b3f771c089546b401dff70d11b35f39c9345f0a079e`  
		Last Modified: Mon, 12 Aug 2024 17:49:12 GMT  
		Size: 60.4 MB (60377758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a84c185b1825709c97051ae98d431ec05d246c2e35c62b32437bf7f15b8489a`  
		Last Modified: Mon, 12 Aug 2024 17:49:10 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:00239ba7660092681bf1ade0ab0e762b6c905f26d8a9d022e73e55e1392bb7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6416708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6533b26091b04fb85d134b608388e0ae62cd36c1c07c41f98b74f4ba99383b`

```dockerfile
```

-	Layers:
	-	`sha256:4ca2c3b9aa62271698d1be5b387f653b15258ec26a042987d5225f1e7d3f2015`  
		Last Modified: Mon, 12 Aug 2024 17:49:10 GMT  
		Size: 6.4 MB (6401777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9828de6fad1b6dac72395f2e472690cbd2d9f22e8def908cdde91c080a55ad`  
		Last Modified: Mon, 12 Aug 2024 17:49:10 GMT  
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
$ docker pull telegraf@sha256:5c87b2f498fa551ab0164c07777e1df21512153e3535eaab4f22164ad0896ea0
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
$ docker pull telegraf@sha256:db955b6f6e5d697a24fe1655ac0c20296527ac44a23436dd00fa39706be5b4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158840614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47dcb17e463f64c992c23fd642e9e2c2259d5e155a9cbde08fb6c151687831e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
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
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef53abc2411c102594507d05da0326efee54a35ea0a832399a3c231758cbaab`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 18.9 MB (18947939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef54e99c1fb93cf2e64602736f7d62bfaa826b6093aaa0543a3714e0f9449dc1`  
		Last Modified: Mon, 12 Aug 2024 16:56:29 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5ea27e8eabae411b9ec797800b59be391907fa47e3c9127354a8a4a133550a`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 66.3 MB (66285397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa599aa3e0f8f0e5b862286162323f1bf0554925852872f0125cdb86cde61d8`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:b6f24294f61ff2befcdb2a80bfd9344aae285e9aec81b1aaee914da6200aab2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6414876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2071c80837710be49f8d8b7f93122f10940b10131bf56e29323d3ea7ad63b28f`

```dockerfile
```

-	Layers:
	-	`sha256:c9b840baaccc3dec7c803b551cdd913200ebc48b18ef60be1cdc7e2d2aeab75c`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
		Size: 6.4 MB (6400250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98dd4b3983ef5a196027bd2fc2ee9798c9fe98534ddc285ab4915ebd588fd82b`  
		Last Modified: Mon, 12 Aug 2024 16:56:30 GMT  
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
$ docker pull telegraf@sha256:36f588bdc36bcec7c4043ceed4c930969c7ecd1e930d1a86a89c657d7f1383ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152431766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539353e4a9fad92c41520adea75209798022d6a681535e7fdc91dce0f6bfa71b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:03:32 GMT
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b7ed4c60331ced332bcb048e97f71fd70743fa6ddf845d25299fbd066f9e37`  
		Last Modified: Mon, 12 Aug 2024 17:49:10 GMT  
		Size: 18.9 MB (18870715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9ece39bd7a0cbb5d239333d404288aab076519704cf6335ef02807d84d25ae`  
		Last Modified: Mon, 12 Aug 2024 17:49:09 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05d6fb7e6e26fa86b8e3b3f771c089546b401dff70d11b35f39c9345f0a079e`  
		Last Modified: Mon, 12 Aug 2024 17:49:12 GMT  
		Size: 60.4 MB (60377758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a84c185b1825709c97051ae98d431ec05d246c2e35c62b32437bf7f15b8489a`  
		Last Modified: Mon, 12 Aug 2024 17:49:10 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:00239ba7660092681bf1ade0ab0e762b6c905f26d8a9d022e73e55e1392bb7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6416708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6533b26091b04fb85d134b608388e0ae62cd36c1c07c41f98b74f4ba99383b`

```dockerfile
```

-	Layers:
	-	`sha256:4ca2c3b9aa62271698d1be5b387f653b15258ec26a042987d5225f1e7d3f2015`  
		Last Modified: Mon, 12 Aug 2024 17:49:10 GMT  
		Size: 6.4 MB (6401777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9828de6fad1b6dac72395f2e472690cbd2d9f22e8def908cdde91c080a55ad`  
		Last Modified: Mon, 12 Aug 2024 17:49:10 GMT  
		Size: 14.9 KB (14931 bytes)  
		MIME: application/vnd.in-toto+json
