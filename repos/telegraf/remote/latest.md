## `telegraf:latest`

```console
$ docker pull telegraf@sha256:74fa2ce3d3e0eba543bf67d022c1c6bd7e7716f0cabb53641b5696a4bd915c6f
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
$ docker pull telegraf@sha256:17b8db94dc0db85b9e63b5854186dd6814604cc062315ec6cda62eebd95b197f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (172992401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d909a4eb1b3349f8d033f3a16e144b2544a748098322efb34072be188aa825eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:08:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:08:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 03:09:38 GMT
ENV TELEGRAF_VERSION=1.38.2
# Tue, 07 Apr 2026 03:09:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 03:09:38 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 03:09:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:09:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 03:09:38 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33783d9cba990ea068fd7b11de7ac26da4e0e7e412f7802b50d66f837c8f77e6`  
		Last Modified: Tue, 07 Apr 2026 03:09:23 GMT  
		Size: 18.9 MB (18944499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2914360d962562f729d89e57142ce9620abe1fea7f9f9064b300d64ecfccbd35`  
		Last Modified: Tue, 07 Apr 2026 03:09:22 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f21f12f1a5be3b7b94fc249297def9dc29522f795c5133f18b6a232fdbd1b9`  
		Last Modified: Tue, 07 Apr 2026 03:09:58 GMT  
		Size: 81.5 MB (81515133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063d9ba824d7baba0fc96f43b2b2f68552320f7aab90377d104b7aa5f4e15ab6`  
		Last Modified: Tue, 07 Apr 2026 03:09:55 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:901c98af60f94359ae6148a5b61b028c6eedcc2281739ab6896b1e229f7ce122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f01e105f8304a9be0d4072b1cb915fa618282ceab9001c4b46dd5410627b10d`

```dockerfile
```

-	Layers:
	-	`sha256:cb15165e332ae744a86b2b698d6d36a9e1b59392effb48116d1c512840516a1a`  
		Last Modified: Tue, 07 Apr 2026 03:09:56 GMT  
		Size: 6.7 MB (6675306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517668c9c7cb30a0989eb10ec5e2e58abaea85698ac205cf4ccf3dab2b091cd9`  
		Last Modified: Tue, 07 Apr 2026 03:09:55 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:73eb27b50ecd1d595f8e376dcabed624247fb6409d6ce68605b6f3dd0ba3ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159178851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbcfba407b4d2a60bf7018485a3544151914ed4f06aeafb80f9f66ffca88c12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:00:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:04:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:04:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 04:04:43 GMT
ENV TELEGRAF_VERSION=1.38.2
# Tue, 07 Apr 2026 04:04:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 04:04:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 04:04:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 04:04:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 04:04:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a99a9abe3964725d9016ffc8402d9cffc28e94f404db8e764ca9583f2090145e`  
		Last Modified: Tue, 07 Apr 2026 00:58:42 GMT  
		Size: 44.2 MB (44207817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2a6632e49a08fc68f1ee0ec0fb4b6f38a03db30dc5ff33b611dc705110ee36`  
		Last Modified: Tue, 07 Apr 2026 02:00:47 GMT  
		Size: 21.9 MB (21942083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7064aee1b881fe04020815950097ba6772db2636b02e8935f9c796a09e796a79`  
		Last Modified: Tue, 07 Apr 2026 04:05:04 GMT  
		Size: 17.7 MB (17699660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9900d1dbddf68ca748bccdf8d31399c4ca7dc7ea5b3c55162425bb6e089b125`  
		Last Modified: Tue, 07 Apr 2026 04:05:03 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393b0bb5ab0f51cddec2eddf26669b13eb02c3b9983b6462412ebe82b5b32aff`  
		Last Modified: Tue, 07 Apr 2026 04:05:06 GMT  
		Size: 75.3 MB (75323599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2c2d5867bde037f0b47e61bd6ffd30115b0990bb4380e909484972b1b750c`  
		Last Modified: Tue, 07 Apr 2026 04:05:03 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:8c4c66654609a89100eef26c438f4577c0c3174e56fb7de10c3ac8bca88b74d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676e28d9f450becb09d5169b4ea63eb95d8d35fa476521fc9e84344bcf1f8546`

```dockerfile
```

-	Layers:
	-	`sha256:9957d7ca43a202adae172de2acf656d58953b46d5afd8db2f4749cb6181d4821`  
		Last Modified: Tue, 07 Apr 2026 04:05:04 GMT  
		Size: 6.7 MB (6669911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11abba1d2c7436d90ee2bc25b60a3238a2757de4a91846db7f9ae8b77abd1cc`  
		Last Modified: Tue, 07 Apr 2026 04:05:03 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3d7c496c2bcb9590de0849d0d3d70bbcf157d0c9cbef9ae9dfc1830a91a15621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163724198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164847084d33466f2bf9d1f8f00e29cb7f32daec30e6f4e341271393a27bf425`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:20:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:20:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 03:20:27 GMT
ENV TELEGRAF_VERSION=1.38.2
# Tue, 07 Apr 2026 03:20:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 03:20:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 03:20:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:20:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 03:20:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053aa2f9ecb5253e7f30ffdda533ae9361ea13704b633656b1038c8af8b5ec87`  
		Last Modified: Tue, 07 Apr 2026 03:20:49 GMT  
		Size: 18.9 MB (18885921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49086742a58fe18731758318a8d8c92bcb86f8fe223c0b2381630a55ae284cdf`  
		Last Modified: Tue, 07 Apr 2026 03:20:48 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d204d82c3153763626d0596b405467834c7a2c3308e4258b90de7de44948aa4`  
		Last Modified: Tue, 07 Apr 2026 03:20:50 GMT  
		Size: 72.9 MB (72854613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41550f6dbf91ed385e676570e8b5450dba4252bd1ebeb3dccc7277c9e5cbb3b5`  
		Last Modified: Tue, 07 Apr 2026 03:20:48 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:4b27d1b213c48659610976f3a14fa75495ef62b4c69da25a18623903a676d22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7324c416edb25f1de66cb95c043b7229c62b2636257de46ce07b3315ed29ea3c`

```dockerfile
```

-	Layers:
	-	`sha256:393e1eed36170b31e4170499743574ce62ba19d3e131e28e4bbd1981ec192389`  
		Last Modified: Tue, 07 Apr 2026 03:20:49 GMT  
		Size: 6.7 MB (6675994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c154c7bf13b7ca0105a6cb1205162bc1ae5eb9d34a0622f97e0e624199fb1d6d`  
		Last Modified: Tue, 07 Apr 2026 03:20:48 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
