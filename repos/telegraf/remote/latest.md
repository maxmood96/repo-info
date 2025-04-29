## `telegraf:latest`

```console
$ docker pull telegraf@sha256:b6408072c5f1b2673b70cdef979ee7f7e06dae14d0c02c294e82a09d5586abe5
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
$ docker pull telegraf@sha256:470afda2dee3bbcb48930508506619c26991a2b0531e497c72a839b19d41fb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169441668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672eceb4fef520816025d014d9a0f6aa262f6b53d9fb6032d07b725822801753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENV TELEGRAF_VERSION=1.34.2
# Mon, 14 Apr 2025 17:23:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 14 Apr 2025 17:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1221c1845b5f5070ef67c42e673a7cff87ed2451df2a915d14b9e0bc508a51e9`  
		Last Modified: Mon, 28 Apr 2025 22:23:02 GMT  
		Size: 18.9 MB (18946203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb8aceb453b0d64609efef1df15de796c6c83926f3fab97618b1b589b7e72b6`  
		Last Modified: Mon, 28 Apr 2025 22:23:02 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a62de3123cdfd8d4e3d1b60bba38cef6648efb927eabef2c6064a5603899b`  
		Last Modified: Mon, 28 Apr 2025 22:23:03 GMT  
		Size: 78.0 MB (77990680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e338fde977d6533bb8bfb3a3c3a939b09576b038e40812898afd5421c73b2d`  
		Last Modified: Mon, 28 Apr 2025 22:23:02 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:628bd480a3575f20b23db85541a69c5023176a0e88f29f02beff755245346792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6457787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77613c68172d7cd9f386a96853d266d66057b5bbb9d423ec249fad42fbde7abe`

```dockerfile
```

-	Layers:
	-	`sha256:db46e11a45983c04b244e2d823d4b8ebc77d6ec518ad1e095102897fb354881c`  
		Last Modified: Mon, 28 Apr 2025 22:23:02 GMT  
		Size: 6.4 MB (6443015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74c4684334e4c7eacd69e76465ef3d217985478dbb48f2b52d888e001afe7be6`  
		Last Modified: Mon, 28 Apr 2025 22:23:01 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:05ec55e2998ebdc68b85e850a9339362eaba7948182957529111a9ea01b66729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155600391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffa21c3c8d5ccd1ca47a95a82f411b1908ef1e0ab44311cf80045750ee5261d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENV TELEGRAF_VERSION=1.34.2
# Mon, 14 Apr 2025 17:23:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 14 Apr 2025 17:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Mon, 28 Apr 2025 21:15:27 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Tue, 29 Apr 2025 03:37:10 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabe566c6af2691f3105823447ac937c1f11b004965e6abc01575a064a841148`  
		Last Modified: Tue, 29 Apr 2025 15:23:39 GMT  
		Size: 17.7 MB (17724705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d5c5bcea6d97d32d23b37764468583109ef0810d01e6d83a881b0023fe34ef`  
		Last Modified: Tue, 29 Apr 2025 15:23:38 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f780af2cef5ea292767820d0c65caf47a60e87a9f68fca6851006133e8e76cb`  
		Last Modified: Tue, 29 Apr 2025 15:25:17 GMT  
		Size: 71.8 MB (71757833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8192cf55a4195c6d7eea6bc39ec4d7976b53b33de2bf3f975bf9e816a029287`  
		Last Modified: Tue, 29 Apr 2025 15:25:14 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:7837740380c29728f06243ed201cc53b330e30dee83dc4502d47b90de7ac5539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6452484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de97903b357c0786bd2e5328d75c225e8faee4a5e2ab31c1d24c2f06d951b0ab`

```dockerfile
```

-	Layers:
	-	`sha256:f48ced50e339b1cd9aedb8a30a02f08d80a86c5566c86799338d1088b6059894`  
		Last Modified: Tue, 29 Apr 2025 15:25:15 GMT  
		Size: 6.4 MB (6437618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c31ddc5dd2ad12a2591446574695c5951d87f718b18279edb963d67cf842e47`  
		Last Modified: Tue, 29 Apr 2025 15:25:14 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4db496c56367cb8ad48e9cbd34f80b7584c6cd928b7ceaabc19de3ec34afb953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160998981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2521ce55cb4ad77972ebc15835dde0812cf4b80e854eb61e12ac1c79d4665e02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENV TELEGRAF_VERSION=1.34.2
# Mon, 14 Apr 2025 17:23:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 14 Apr 2025 17:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7446c58993d11b00fcf70a65c363df298c8fd24914c3657943f2362852a75e88`  
		Last Modified: Tue, 29 Apr 2025 19:27:33 GMT  
		Size: 18.9 MB (18871759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38670875debfb321519f19305350d13646a48ebaac8d2b798ab7aa84cefe61b0`  
		Last Modified: Tue, 29 Apr 2025 19:27:32 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ec0acd2d79ae0af3c87fa5d8728a3905bba96a51a7d14f6d80dbc699c41193`  
		Last Modified: Tue, 29 Apr 2025 19:28:35 GMT  
		Size: 70.3 MB (70252909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11614f4b96feec840c7fcfea888aae3e841ceaadcf56772bd07605ad3653b46`  
		Last Modified: Tue, 29 Apr 2025 19:28:32 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:4960e99ceefe73669254579ef259a90364b5b70d789e7391ef46099ff3349f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6458597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72375b4047e7c0bd12fc239e094e233ca4a423b7ddb235326c8c19d3bea7a0d1`

```dockerfile
```

-	Layers:
	-	`sha256:b8740e869f2aa1e62650cc427c3faac38662ca8bf62602d778b6e552afc62892`  
		Last Modified: Tue, 29 Apr 2025 19:28:32 GMT  
		Size: 6.4 MB (6443703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd3fa9092e71045544b4836d7bfac305d6868bfcc4a243ff2c15b60e3175cd1a`  
		Last Modified: Tue, 29 Apr 2025 19:28:32 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
