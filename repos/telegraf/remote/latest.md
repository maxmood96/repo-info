## `telegraf:latest`

```console
$ docker pull telegraf@sha256:69b159d950bc6b13f2a0ddba38a3134d48846e25c30939b6337d793a0f7c9be2
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
$ docker pull telegraf@sha256:e396e6b0fc235d80c69a2737e6d303c8178034c19d935fa4646cb143b99c22b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154599417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1463988fb9ac4d7f92622e154f20a430349ceb8e9d80ad5c6c7480e42586e3eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76047489d0b2ccdc4598bd413a2f7f8cddf3685229a8c8d2dfea4e28147e471`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 18.9 MB (18948018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c013e6ebce0fe5838f78b11b747a7ae2fffa092cdee0749609bfac6ae129058b`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049270f6c151d3bd1e976b0ca9a6d3aaabe9c2cb5ca253cb53edfb086182ecfb`  
		Last Modified: Tue, 14 May 2024 03:58:26 GMT  
		Size: 62.0 MB (62022501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1cf419edd6c5b8dc261f09c429795709ae8ec676035b9432f2635a6aa7a94a`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:82aaf3de49fedf1eb53867ae333b120a5baebce276115a08001a49cb66e0ec6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6312805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeeb6e6fe095a30e3ff49b6266c69beaa7f85fc9dd7290d1eef8c3bc33da59af`

```dockerfile
```

-	Layers:
	-	`sha256:b2533c5a707801d71bd284a7fabafe70b0371175da6b354e741a5f639fe0f9d7`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 6.3 MB (6297897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6d8718e9191bd392eb11b4485e6e87d2741437935af64356b66f9dd76f93338`  
		Last Modified: Tue, 14 May 2024 03:58:25 GMT  
		Size: 14.9 KB (14908 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:861cad69a8575e4398659584abf36da784e60f2166dfa6dd6ab7790bef3248bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142267582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e855130a8d931154c4f6c1f4350381ec07f07490b51100e77c1af9c1aff9247`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:1e106a38a0e44ca74d4d29c6d797780e7a29ffe249e473c48ee2aea553fc013b in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:dfc3b4ca62816a9cbf2bdfbdd78bf692a522e7f48a280492b9f87d55b2f4aa2e`  
		Last Modified: Tue, 14 May 2024 01:12:21 GMT  
		Size: 45.2 MB (45174745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d6443415d538c3bf0e0d6ecc0f6b7603b4caf6c79708d0670bc082e9721c5`  
		Last Modified: Tue, 14 May 2024 01:46:47 GMT  
		Size: 22.0 MB (21953893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901b8b18d82e5b57b89385ec062d1674265344d73cca05bba989b96a6cf4f07a`  
		Last Modified: Wed, 15 May 2024 08:08:19 GMT  
		Size: 17.7 MB (17724872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6537ab1b98b6a7364bac3f994ad624855097573d29bfa741f0a5f24eaffe2bc`  
		Last Modified: Wed, 15 May 2024 08:08:18 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ead9ae2660f91eed96f1d79fba91355c4e402a7587715ade07eac2499c612b8`  
		Last Modified: Wed, 15 May 2024 08:10:11 GMT  
		Size: 57.4 MB (57411665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bf44587aa91549d6fa3010c24f7d6126a7cad150158c70a20a75f03eca7f27`  
		Last Modified: Wed, 15 May 2024 08:10:09 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:0e4a9e210b07a4206cc24aa457d83d0feefa9ca48795f8141d4fcb5611c6f06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6307924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1976756e64060f98fb9dba49f34eea8555a1515630f70f78407b411b1667bd53`

```dockerfile
```

-	Layers:
	-	`sha256:cb18553624107a0dade30a7a5419bce01fe5c565e1a979beb815ac528a1f8287`  
		Last Modified: Wed, 15 May 2024 08:10:09 GMT  
		Size: 6.3 MB (6293259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4342604b80bc9b3621345c2bf45f41e94fb37c749cb4b89b6d24158440b03fd6`  
		Last Modified: Wed, 15 May 2024 08:10:09 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:dc285c64c639cb3993623643784b64e8a4eb29fdd7e561392536680fc90ec024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148491928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74c8fa2cc4a8a07803bf758ee67d85c18c9051c40706d01d0fb02808ba3f21c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Apr 2024 19:40:36 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 22 Apr 2024 19:40:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 19:40:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Apr 2024 19:40:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Apr 2024 19:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 19:40:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15856ca26414127b85cee6d10acbc4cee6eba9070f3f5a04b9cc72ce95abfa7f`  
		Last Modified: Tue, 14 May 2024 01:52:50 GMT  
		Size: 23.6 MB (23586610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787c90cc4c220f2efc01fd1f87a403a247f61d1030f562e906930332d905ebdb`  
		Last Modified: Wed, 15 May 2024 15:06:57 GMT  
		Size: 18.9 MB (18870680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23862d11452a5b51a68997e785996fd1e75da32dd2d37041a0da1bf5f6d58f9`  
		Last Modified: Wed, 15 May 2024 15:06:56 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f5b2f977b6036e43d45ac328a1a646692436a19ee090827e11ce5c9edcb669`  
		Last Modified: Wed, 15 May 2024 15:08:14 GMT  
		Size: 56.4 MB (56418842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964c37ace22facb6bfe9da91163c8ff2779ca16061b525ba3fb79623a50b0ded`  
		Last Modified: Wed, 15 May 2024 15:08:12 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:aa974f9879183e557fe369bf29ba54f63458134f93cf6eb6a3d4d79d75e1cd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84e896a43c7ae06246fcbeb100d25c808617c468278b560781f7177433c16a8`

```dockerfile
```

-	Layers:
	-	`sha256:0cc274d06a679f1c2f3c878905c8db64c939574be5d6d754ecb84af1e5251eed`  
		Last Modified: Wed, 15 May 2024 15:08:13 GMT  
		Size: 6.3 MB (6298512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c952198751eae6e80283c250236fcf72e68882034afcb521b5d7a35980a159b`  
		Last Modified: Wed, 15 May 2024 15:08:12 GMT  
		Size: 14.6 KB (14583 bytes)  
		MIME: application/vnd.in-toto+json
