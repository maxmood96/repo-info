## `telegraf:latest`

```console
$ docker pull telegraf@sha256:c4d0805cd25432890dc14e2119d7970f5838817bc43319884bf2cb41bf60f52f
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
$ docker pull telegraf@sha256:80f0262f1764d7220207e02d4f39e2e4746a57836865f95339121c2f5d4b9319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (174991948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c60b6e1594923a92cb94407321531d19377b3f65ff3d0f2b9a13618f5234b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:53:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 11 May 2026 23:53:45 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 11 May 2026 23:53:45 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:45 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc401cab11768d2b73aa0f36b0d76831b9aa4c7a568fdf9be0fa309112ef4fd4`  
		Last Modified: Mon, 11 May 2026 23:54:06 GMT  
		Size: 18.9 MB (18944282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bf251f55455c38e3f15bed7a3f75b426f1815c5d0dce73125a3617fc770a62`  
		Last Modified: Mon, 11 May 2026 23:54:04 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a720032e9b8bdb47e8f616671f2022496c72cf16644ad344541cf9d2b135a92`  
		Last Modified: Mon, 11 May 2026 23:54:07 GMT  
		Size: 83.5 MB (83511119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c19c791a0de19bd603e238311b3d1fa63543a036ff1f69d222c7e7b1dce41fd`  
		Last Modified: Mon, 11 May 2026 23:54:05 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:55cbed9339d919070e63e8ec47800577b2df280770b0f6afc723190d297a3a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6689294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4934a5127878b8d5da77a4ceb933d0c592f8332e1119e4d02ebd3205ad434146`

```dockerfile
```

-	Layers:
	-	`sha256:febb6e9adddc67a1c7ad1bc75bfbf4884cc6b32992f68ebd4f2cb60a9ed0a7e5`  
		Last Modified: Mon, 11 May 2026 23:54:05 GMT  
		Size: 6.7 MB (6674565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab5e4877b539a3bedcb6961e259913239cd77f99ba352bf3cb774d5fb4da89c`  
		Last Modified: Mon, 11 May 2026 23:54:04 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:07efa659c079d4c9943ff648642b91e78f59ea97033344fa7aa66c0455b5a775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161292585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f9f10d80e2b6c5b34662d466df5df504e51a7e6efd801626bc64c09ae727b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:46:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:46:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 01:46:46 GMT
ENV TELEGRAF_VERSION=1.38.4
# Wed, 20 May 2026 01:46:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 20 May 2026 01:46:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 20 May 2026 01:46:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 01:46:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 01:46:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61246c0a5a0fe9fe8cdc1bfde0fdfa49ffafcc94cba31f4aecc0c34bc346064`  
		Last Modified: Wed, 20 May 2026 00:02:11 GMT  
		Size: 22.0 MB (21950133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca4eee7f25cd54245b4e70cb43ccdc8cf464cb8820d3e9bac05a2492e0817e0`  
		Last Modified: Wed, 20 May 2026 01:47:05 GMT  
		Size: 17.7 MB (17699709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a980b0e2df8ee33765f5df04291d708c696661126237c8967fc0b4816f7c650`  
		Last Modified: Wed, 20 May 2026 01:47:05 GMT  
		Size: 5.1 KB (5068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c6b201437b9e75c48613c63b169c95d3f5a1481f62d902dad1cba11696a638`  
		Last Modified: Wed, 20 May 2026 01:47:07 GMT  
		Size: 77.4 MB (77427900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26c2218f05f003d938a8f0b53dc2ebc1ca4e0bc5e7cb468590e7c0a063841d8`  
		Last Modified: Wed, 20 May 2026 01:47:05 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:a7cbba2264587bc88f4091a7662693bd953d2224ca1a6c07724f2286505d05d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a199a383d5671cdd5694bd908ecd4da41521b6aacf0ed1d3b22f7b65f40a69b`

```dockerfile
```

-	Layers:
	-	`sha256:aadd75fa4eacf14b8c1105a9ec227f26d09cc6a0faf944ad4312fa17ba28361a`  
		Last Modified: Wed, 20 May 2026 01:47:05 GMT  
		Size: 6.7 MB (6669188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc902db08cc1320eb0a702606517c6b0130b111767a9eab0ce6c030ee97ed60`  
		Last Modified: Wed, 20 May 2026 01:47:05 GMT  
		Size: 14.8 KB (14826 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b701b1e13950d8f9adb53066f63432ed67662de69a4c6f45cb2e814f4566e7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165361181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db91532e2304fc092c7ce07e5aad20f305ec392acb4cbceb05dde5fdd6e79bb7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:41:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:41:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:41:05 GMT
ENV TELEGRAF_VERSION=1.38.4
# Wed, 20 May 2026 00:41:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 20 May 2026 00:41:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 20 May 2026 00:41:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:41:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:41:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b0db6fe1f2805539a2c29b2be8827946ac0cc6de09bde559a1626d9c21028`  
		Last Modified: Wed, 20 May 2026 00:41:25 GMT  
		Size: 18.9 MB (18885919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606071820b024c6f1f9751ec5becffbb43d32bba0a21d6615b6f98dc3bafc70d`  
		Last Modified: Wed, 20 May 2026 00:41:23 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f36a226b196a8456634158533c07328112710593194b8b4e70eb4e9aba6a44`  
		Last Modified: Wed, 20 May 2026 00:41:27 GMT  
		Size: 74.5 MB (74476757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b931f16d2dd094d06f4acec9c4a66c780666e0586c10b05a68605f8dc51b10`  
		Last Modified: Wed, 20 May 2026 00:41:24 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:fef566dec8821a46c8ada35b57d405b948aa940eebe7b4a8f9d7219f612e5f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db6d5363a24809490a4d5272bda10be8624d51052a0f0ab895ca767c79a3c5f`

```dockerfile
```

-	Layers:
	-	`sha256:49ee1a9ead2c3ddbbbb24b4e5d367a201ac9a37b5d5c95033ccebc5e83baa069`  
		Last Modified: Wed, 20 May 2026 00:41:24 GMT  
		Size: 6.7 MB (6675271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d0d50465488a0de90d508b1da4af5953d15ee447ab302c981e510f9038da065`  
		Last Modified: Wed, 20 May 2026 00:41:24 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
