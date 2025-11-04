## `telegraf:latest`

```console
$ docker pull telegraf@sha256:532feb6341c2eb835eac808160f3011f3e5b0f87cb05e53797e6c98e107708dc
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
$ docker pull telegraf@sha256:0eccf97c41df048cd65c5fda6e277509513f363409c01eddb7f12fb8d0e6d92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171811238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0aab2138b5e5435b33d5d10b7e074b1c2788a205f0f167c1daa4b67f12111c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:29:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:29:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 04:29:37 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 04 Nov 2025 04:29:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 04:29:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 04:29:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 04:29:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 04:29:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb445e472b1bad54f5a28edd51b11aec79eca8513394866a261891be9da6a343`  
		Last Modified: Tue, 04 Nov 2025 00:28:00 GMT  
		Size: 24.0 MB (24029301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29cf6fb1834bc56f1820d5c84abc85f28695e95209a58393b1b26c9be121e69`  
		Last Modified: Tue, 04 Nov 2025 04:30:05 GMT  
		Size: 18.9 MB (18942926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b539859c7750f1249bb257b45a45b5f5ae305336e7bb8d90ac7a4d85015853f2`  
		Last Modified: Tue, 04 Nov 2025 04:30:03 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de777dc026ca1f1c8a52009c786da780f79b0974fe24d990991d63a040798c4`  
		Last Modified: Tue, 04 Nov 2025 04:30:11 GMT  
		Size: 80.4 MB (80353890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd426182f8e9b22e08d9c77eb985516563b545b8b4e72c57d5927d1863ecb0d0`  
		Last Modified: Tue, 04 Nov 2025 04:30:03 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:2dd6d812624bd07bda519a13abfb5f323108fdce3db208ee678b61716383c4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6667434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9e2c337067463aec9c7fbb04e06c7038082371a84ae481c582d5b7b0e84d65`

```dockerfile
```

-	Layers:
	-	`sha256:214abe2901caf515feb72b6094317cc8b5156f2a540371abd1a0f73d6aee0f5f`  
		Last Modified: Tue, 04 Nov 2025 10:10:57 GMT  
		Size: 6.7 MB (6652705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:773612aaa5d3e5bd971e2a11ee5d3fc63d82b5b9ee67047ed48660ab1e2d1b59`  
		Last Modified: Tue, 04 Nov 2025 10:10:57 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:d665d3ec2da8e0875403b8e3acba6dcba67b59146e072f31cc012e82d5ff038d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157763649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066b7460db2684c096d017a087ba33208afc64b6edbff3db8b555f6b102f9532`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:39:04 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:39:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 02:39:43 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 04 Nov 2025 02:39:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 02:39:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 02:39:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 02:39:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 02:39:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:461f215c759f019a0fb4d33c976a91c4c2e4b033762b07a2f81bac66dee9e613`  
		Last Modified: Tue, 04 Nov 2025 00:12:30 GMT  
		Size: 44.2 MB (44196437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad602f359c1ad647108cc57270e592fc1f62f8ffd947a100fecee62a4a0d017`  
		Last Modified: Tue, 04 Nov 2025 00:39:15 GMT  
		Size: 21.9 MB (21934879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5207eacc0a636b8c0b0753ace942e14c051938d7aac0efb93c5a8a055bd312`  
		Last Modified: Tue, 04 Nov 2025 02:39:34 GMT  
		Size: 17.7 MB (17722410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00102ab6e81a9d64a6dbc8926419879ef6abccddbf68907fdbfc2a34a1f5dc0`  
		Last Modified: Tue, 04 Nov 2025 02:39:33 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60591fa952c11ef51933b7620508c7dd6f22a817271d52648335ddb4ce4bfbaf`  
		Last Modified: Tue, 04 Nov 2025 02:40:12 GMT  
		Size: 73.9 MB (73905858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f99c9819e7307c39d86bed080f060eeb5702546aa1eac4f5af47d9b9ad72da`  
		Last Modified: Tue, 04 Nov 2025 02:40:07 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:bcd463f3e90460200222d69e02e4009c91a797217c0f23e54a32aef67a83697b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804a4a55b056299edb7b984c408f203a2843ba6665899dd851c480282cee3a1f`

```dockerfile
```

-	Layers:
	-	`sha256:94f71825792615d055ebf7128970d032049db252208ff814851cf9892959aafc`  
		Last Modified: Tue, 04 Nov 2025 10:11:03 GMT  
		Size: 6.6 MB (6647310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93098f53e840a56d2933448aaf8de66a10e1e7b620d2e8ff9e7a56e80a867046`  
		Last Modified: Tue, 04 Nov 2025 10:11:04 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:77821a3b64585c47d06a94fbb482b55ab9d9d61e17de611c384d489545600fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162542379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cac55e111a130abb2ff7feae1dafd6a9cc179514d562c696921800942737cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:43:11 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:43:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 01:43:18 GMT
ENV TELEGRAF_VERSION=1.36.3
# Tue, 04 Nov 2025 01:43:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 04 Nov 2025 01:43:18 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 04 Nov 2025 01:43:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 01:43:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 01:43:18 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463896571d3ff5317461a64229e9e4cb27d6d877114079419cf8b4fc96b0c02`  
		Last Modified: Tue, 04 Nov 2025 00:30:33 GMT  
		Size: 23.6 MB (23598514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c9d59ad07179a8b0bc11da6ff910f4e751034bdf10bc03cb10f471d4dcfa26`  
		Last Modified: Tue, 04 Nov 2025 01:43:48 GMT  
		Size: 18.9 MB (18884193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d744edeb94bccdc025987feb82d5cf1c9ff0891355078bd049854bf32f85c9`  
		Last Modified: Tue, 04 Nov 2025 01:43:43 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c431dc7814280cfeac572c62ebf1bb79c797363cfc8f840e9c09f5891f253e`  
		Last Modified: Tue, 04 Nov 2025 01:43:49 GMT  
		Size: 71.7 MB (71696117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276c544e3a2d3349d4cc60169e6c49066766fd34b505119c53b92d06e130929d`  
		Last Modified: Tue, 04 Nov 2025 01:43:43 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:6f9676fd40264a609bf14834028aa5224af90b4abe27a36374f715e7a199ab41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6668244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1069351a285bc6288881d43209281d63049e94433d0a883905231c3e1c5470`

```dockerfile
```

-	Layers:
	-	`sha256:a90aeefb3f8b624abe0dbf283181184b613d8c398b731a488b37a398abf05f9c`  
		Last Modified: Tue, 04 Nov 2025 10:11:10 GMT  
		Size: 6.7 MB (6653393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cea634030cd9efd95c9adf2c31b3e1d45218270c9eb8efdc49a92c7fb470bff`  
		Last Modified: Tue, 04 Nov 2025 10:11:11 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
