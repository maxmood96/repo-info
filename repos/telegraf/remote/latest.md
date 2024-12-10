## `telegraf:latest`

```console
$ docker pull telegraf@sha256:1b231178e42486a349a937bb469c7b0057979657fc4f7478598373e14635edbd
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
$ docker pull telegraf@sha256:f5d75cd8943f1f3927c20cbaf69bb541a0c0f21db5b9a87e82e2aeff0aab3f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164337836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b0eff2abe3c880907ec09cc86666f55ccfa20fdf052547ce740e7c795d8b0d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.33.0
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a1a61d9f4ee7645baa168af976c33bcdb6db4c60ccc12c816992fcb1a66c73`  
		Last Modified: Tue, 10 Dec 2024 01:29:23 GMT  
		Size: 18.9 MB (18948074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150cdea4328a2349912cc4adc99ba756d0f6f91884b3bf2d34eeb5e993d957b5`  
		Last Modified: Tue, 10 Dec 2024 01:29:23 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dccbf029dc3bd9c799fb200bfe8c3137394115ddca14d1fe634d6d868427278`  
		Last Modified: Tue, 10 Dec 2024 01:29:24 GMT  
		Size: 73.0 MB (73024281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf6a9e715edf7afa2559e97fb26ced4f0ccd355547f5a06852fc85d7dc6e928`  
		Last Modified: Tue, 10 Dec 2024 01:29:23 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:83d58cd5f93b008e4838cc69050cc75b0105860ae53b83e10b79e8bb70f11148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6451805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b5fb0764af50a1748faf2de2196c37f360fdb7d23a7135789fe19fe420e95b`

```dockerfile
```

-	Layers:
	-	`sha256:991384b93cbdb521b9392011b19b143c3e8a226ffc0ec0de1b2ea4448aae0b6a`  
		Last Modified: Tue, 10 Dec 2024 01:29:23 GMT  
		Size: 6.4 MB (6437033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75208fad75fad2e62315e1d9d7e616bd18057f1cffe957ef614abd54fe0d0ca1`  
		Last Modified: Tue, 10 Dec 2024 01:29:23 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:e5b27c2ef3ff482a3ee0969d8c54c8fe2f173d3b4d7141655b912d8827216a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148377956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb61d35d6948bbe2265f18e9aaf9ad0a2a346f3273cdb09de5cde3d3e4f7c1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 18 Nov 2024 20:48:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4d43724a324f138c88a78ca6df0a39ab6868bf1f121eb974439c5a51284e1ac2`  
		Last Modified: Tue, 03 Dec 2024 01:27:59 GMT  
		Size: 44.2 MB (44200109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0e53b92c3d0f5c370d71aeac1be1d23e475f1afba41d896ace0ff6eeefc90`  
		Last Modified: Tue, 03 Dec 2024 07:36:14 GMT  
		Size: 21.8 MB (21767161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a0fae665182d09938f5537e93b3ed9eae9bd1b5abe0f7ef912d2edad66d41a`  
		Last Modified: Tue, 03 Dec 2024 19:05:53 GMT  
		Size: 17.7 MB (17725368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f9f8c25a5eb566f3fdae38a3011e5240ea0ce6ef1bf09521da0022dc076eea`  
		Last Modified: Tue, 03 Dec 2024 19:05:52 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdad1552b68f7391dc48f1d97c8626bf76dc44bf481f8764dd926cf22365790b`  
		Last Modified: Tue, 03 Dec 2024 19:07:28 GMT  
		Size: 64.7 MB (64682909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad4217e5b9a0fb2ae673d7fe09dfe787a41902758310706fb116fc17ba9c945`  
		Last Modified: Tue, 03 Dec 2024 19:07:26 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:2ff43579636ba3cdbe00b9ce6592d5761bd0f8bc89a74ff4b6c32a7da249a799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6437293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dfa45862a61d90a27a30e0d601b244d2ad8f40a6bfe8a7dc8606c168d7407b5`

```dockerfile
```

-	Layers:
	-	`sha256:89a073ebcafcee627c6c5f91eaab6af9ec7495e6f458417ae64cf8e0e22a47ad`  
		Last Modified: Tue, 03 Dec 2024 19:07:26 GMT  
		Size: 6.4 MB (6422427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b438c3147e2b17fdeadbc9ac847a42dea871c053b11f5396ff42b6c12be9daf`  
		Last Modified: Tue, 03 Dec 2024 19:07:25 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:40e41ff39147e8f90195a03f8864fa6843b7a228c52b9201920b54aec99c1178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156540648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca3ff266254e80b0d9d10f0f26e0e21078ff7fba03b2497a6d7653cb9591bb5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.33.0
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a070e15373226f4fbfe69c7af83d28e42c1f77ce76ccbbb4737bf4a1da174492`  
		Last Modified: Tue, 10 Dec 2024 01:39:42 GMT  
		Size: 18.9 MB (18870708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e95ca01ac71ca5672641d03cfd0c8466bfa4fecdf93e8c5577d2f82f8d2ab`  
		Last Modified: Tue, 10 Dec 2024 01:39:41 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c06dac64b7f90a10ccf8b0d0e5eb0b7901e16156df218a51eda67314341d68c`  
		Last Modified: Tue, 10 Dec 2024 01:39:44 GMT  
		Size: 65.9 MB (65936049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2c07c63809986a0a2194bbdab848c90feac4d413ad7a2c12012227a960c22b`  
		Last Modified: Tue, 10 Dec 2024 01:39:41 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:f165e6c30b1973032889dbcfda7af645f372c3111280bb6d5655e4fb1fe9877f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6452657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea951dcf0488d9f23c0fabe731151bb3fc43f195adb173ee2b4d2ddf8341fc9d`

```dockerfile
```

-	Layers:
	-	`sha256:0c824b538401a7bc0942127446fd2fc6ff7bd7e79b77a818de7b98f29eb41726`  
		Last Modified: Tue, 10 Dec 2024 01:39:42 GMT  
		Size: 6.4 MB (6437763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d7145aecdb76eea458083505cc221b80cf30dd0522be0b1c7cb2169cd88d642`  
		Last Modified: Tue, 10 Dec 2024 01:39:41 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
