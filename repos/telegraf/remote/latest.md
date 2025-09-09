## `telegraf:latest`

```console
$ docker pull telegraf@sha256:bd82f94386b619a6ad22d64f220ea4ce7efd620d002743ee9b1b76351eb80fea
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
$ docker pull telegraf@sha256:09efd7277e074e14f58b6aa50cd107c8abbe6898aa2c2b9029b647bf3fc60fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171241057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:360e8b4feb461261003f6e94145404dea824e7d2d377a10f73c907879a6d8e09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
ENV TELEGRAF_VERSION=1.36.1
# Tue, 09 Sep 2025 01:37:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Sep 2025 01:37:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 01:37:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d1a0f1ddd0803d51fc5f5e8d035ed9a04f06bd2551fff5d94ae9d975432043`  
		Last Modified: Tue, 09 Sep 2025 18:16:58 GMT  
		Size: 18.9 MB (18942917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34061fc6be711b5b2ce5fc1c01a7957a0185335d4f3a072ca25ff5d71720d1c0`  
		Last Modified: Tue, 09 Sep 2025 18:16:57 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35e6b83a3d36081bbc656e054ae64c8f27682b2e806fa1017ce19ca3d4cd491`  
		Last Modified: Tue, 09 Sep 2025 18:17:07 GMT  
		Size: 79.8 MB (79789123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a12c0b1ff0f0351a224730958090f2affd58e5f8240144929ba6a35ead76df`  
		Last Modified: Tue, 09 Sep 2025 18:16:57 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:7771fe69ee44718411df1cdca9e3a15916321f1f1c63238642f96214060bc016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6661775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7fb2ab2239ee79cb670069fc8c329b36181567c19380d1a18c50f8badbced1`

```dockerfile
```

-	Layers:
	-	`sha256:a9aeb94991521f1fa2b26acae8b4ad303da7a09962a20ec3aaf10189f2426ed7`  
		Last Modified: Tue, 09 Sep 2025 21:10:29 GMT  
		Size: 6.6 MB (6647004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec01a023330011a1460d6bbff15171bbc3c3dae60bf4545430b933e395e2130d`  
		Last Modified: Tue, 09 Sep 2025 21:10:30 GMT  
		Size: 14.8 KB (14771 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:b62daece4777f68afeb86ac572c0719ce1920f0225cb566c7f46c228bce469c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157245015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8abd69db5e9022491cfbd154dff628ffb9b3a78248a4d012eb219ef45588c52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
ENV TELEGRAF_VERSION=1.36.1
# Tue, 09 Sep 2025 01:37:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Sep 2025 01:37:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 01:37:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4eebd6ec745dd40cab202b83a14e7cd4152f3f99100f9150cff7f3d0d0483c`  
		Last Modified: Tue, 09 Sep 2025 20:17:47 GMT  
		Size: 17.7 MB (17722594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6044f044ea299cf10447b0a30b7ef9c5979d25ecc0a7caf22693fd490b24e244`  
		Last Modified: Tue, 09 Sep 2025 20:14:13 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88059f84e6ff54be49cf89ee6df34c6a456fbee85dc774372b6f46a2a04cf5b`  
		Last Modified: Tue, 09 Sep 2025 20:17:50 GMT  
		Size: 73.4 MB (73392938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384cd8a48ca40bdee95cecf88c5e28e493fd6e0d849af39e822d024611597bcf`  
		Last Modified: Tue, 09 Sep 2025 20:14:16 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:736ce11dfcbf6173c5a206113704d397d06a1c521f5bdfdde5afbc532a9b197c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236bf2fee099c0671c875e6fead887f27669f674c174a970060e3336187aaf63`

```dockerfile
```

-	Layers:
	-	`sha256:3f52bca9d6b0c47ace8d7372ddd60d717c311d098bf4aba11a33c3045af0c58b`  
		Last Modified: Tue, 09 Sep 2025 21:10:36 GMT  
		Size: 6.6 MB (6641609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4dae873ca86bdf51b45499a2c20ab358ceaf82fa5bd50c39931fe32e6ed9154`  
		Last Modified: Tue, 09 Sep 2025 21:10:37 GMT  
		Size: 14.9 KB (14870 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3149ad39a3a17e6733ff33519ff8094e8e02bad169dda8c83405c8e5d97bd5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.1 MB (162050735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99033132f9c2889e87b9243000d1413aa493466490d9e03e81825e937ae53e43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
ENV TELEGRAF_VERSION=1.36.1
# Tue, 09 Sep 2025 01:37:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Sep 2025 01:37:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Sep 2025 01:37:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 01:37:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe43d44608d135394498a255aba1969a0109ddb1a13b8022aa46f1758acd541`  
		Last Modified: Tue, 09 Sep 2025 18:18:06 GMT  
		Size: 18.9 MB (18884254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1125cac338c28429ea2c95fd9587549a116bc8b1db21ce37e22111cfe412fc36`  
		Last Modified: Tue, 09 Sep 2025 18:18:04 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5f97e65dbee7a67d333e0b0147f73788642052120d99787af9935d1dcff44f`  
		Last Modified: Tue, 09 Sep 2025 18:18:16 GMT  
		Size: 71.2 MB (71210265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572bf6857de30e2971432e5837a4e3ca0de1571bcb100bca76c5f785b31f933c`  
		Last Modified: Tue, 09 Sep 2025 18:18:04 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:7e35cc1d2cc7f74aca8f15d827354a1f7433e44f23c5ab0bf671b74e3d867db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286439372405fe4c0e218f0b16143d7848dae3a8e1e74ec213d0396487db2117`

```dockerfile
```

-	Layers:
	-	`sha256:0eb9755664491d6d806cec9c6618002cd49662344d13bda99f5bbc3afa6d2958`  
		Last Modified: Tue, 09 Sep 2025 21:10:43 GMT  
		Size: 6.6 MB (6647692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40dee4063bc29766c0349ea0df24db8e9ed02824eb5d4a6ff5602664abff5db1`  
		Last Modified: Tue, 09 Sep 2025 21:10:44 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
