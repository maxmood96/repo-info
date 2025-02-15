<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.31`](#telegraf131)
-	[`telegraf:1.31-alpine`](#telegraf131-alpine)
-	[`telegraf:1.31.3`](#telegraf1313)
-	[`telegraf:1.31.3-alpine`](#telegraf1313-alpine)
-	[`telegraf:1.32`](#telegraf132)
-	[`telegraf:1.32-alpine`](#telegraf132-alpine)
-	[`telegraf:1.32.3`](#telegraf1323)
-	[`telegraf:1.32.3-alpine`](#telegraf1323-alpine)
-	[`telegraf:1.33`](#telegraf133)
-	[`telegraf:1.33-alpine`](#telegraf133-alpine)
-	[`telegraf:1.33.2`](#telegraf1332)
-	[`telegraf:1.33.2-alpine`](#telegraf1332-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.31`

```console
$ docker pull telegraf@sha256:c07851474ac4edd079b45750eca3ee6b8954d81736e4d0f5e88018ec56bb069d
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
$ docker pull telegraf@sha256:924a1e8c991087a7ce52a90dfba715c641be38aa497704068707089c6bbba63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157773984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b611451ad13075398bc84f6ee6a28d02583caa13add72a46549a3610f599f218`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.31.3
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 10 Jan 2025 18:06:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 07:11:25 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10a5068bceb1e490674294d0059f3244a8eb6ce7cc94ee00b6564c73147703f`  
		Last Modified: Tue, 04 Feb 2025 07:21:06 GMT  
		Size: 18.9 MB (18948067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b5b447d955db8b7069bc72e6eb4886061a3c646fc910e3da29e1a50ca8b7de`  
		Last Modified: Tue, 04 Feb 2025 09:54:18 GMT  
		Size: 1.8 KB (1778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767cb8b5780ab5a12365e16b784f2b42c75f2db2725aae23c91554819f0341c5`  
		Last Modified: Tue, 04 Feb 2025 12:19:25 GMT  
		Size: 66.3 MB (66285474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710675496ca2e9c84025424670bf8a459ef847a51ec79f4ad40138600647ec9e`  
		Last Modified: Tue, 04 Feb 2025 08:05:34 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:110a7e29d8ab83ee6eb40c178ce57aee08006ed950e87c6726342450b3b86782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6429049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78805e014ac908aaf4d1f741af03d90688d1a61659b85c245606c04b0c7e1f36`

```dockerfile
```

-	Layers:
	-	`sha256:687173db0c71b7075eb4eebc7203842999143979f1956940dcd8af6a480eedf4`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 6.4 MB (6414580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ad2a991c3f0cda7bdd268c33e265acd9b8ba7ce8347743f4462b328d9c866ad`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:80bf9a6198cdddd3e341bb1d843b04d263bcd1c39d3ebe8b2fd4348671a65598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145544334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ecf0158ea08df57a4b96312128c56f68db6f9d82ae9f446054f86bbcf0b80b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.31.3
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 10 Jan 2025 18:06:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 05:02:17 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 23:37:50 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d37da5ea34f101d528e16df8870c72e9bd46b0b2a815871f8b2cad7f226a6`  
		Last Modified: Tue, 04 Feb 2025 22:12:18 GMT  
		Size: 17.7 MB (17725432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7eff7fe833c3fbd6d3c6ddd5c4675fe3df5730fd39b06790f9bf9180f68be3`  
		Last Modified: Tue, 04 Feb 2025 23:37:47 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6e79ba0bf8c0c7e2cec56f584f900184f5281a417f6fe872a33864e846e3e8`  
		Last Modified: Mon, 10 Feb 2025 22:51:19 GMT  
		Size: 61.7 MB (61672360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c309b3a1ce3a10fa77348b583e640083dedac36625f96116e074ff34a55644cf`  
		Last Modified: Mon, 10 Feb 2025 22:51:11 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:60c769fdd167e9ad1a361c0e433ebd9430ae5b3ba1fcbc011ef1b089694bc18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2bcc9ce0c93896239fdf9c842b6754dcc946e4eaddacfdf6fba32ea89c7d09`

```dockerfile
```

-	Layers:
	-	`sha256:d5b7a63d54c86b99c07cd11af6d6be02cecd8da3ac90e710e6ec39a4503f448e`  
		Last Modified: Tue, 04 Feb 2025 18:30:30 GMT  
		Size: 6.4 MB (6409984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c1bf88c1303dab963aa25f03aa55530abbf185f9914e6df4f1c3f3e12cab9f5`  
		Last Modified: Tue, 04 Feb 2025 18:30:29 GMT  
		Size: 14.6 KB (14555 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c746494a8535bfb5dc3bb0005eaa4614e6e1b34379f816a621d95b180958ea2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151155923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403e5a232c73416761ffa300da62f59822199e0af4a1749d6f059923e0b17105`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.31.3
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 10 Jan 2025 18:06:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Wed, 05 Feb 2025 00:14:09 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381030a63d0196bc211f3d91ddb8a25d6e1e4a40d13d2d068d59ee1acc77fe02`  
		Last Modified: Tue, 04 Feb 2025 23:38:16 GMT  
		Size: 18.9 MB (18870740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5c3c63ca133a2a6f025a1cac4edbb065fe2fa04d4cac68f1f4d1aaa01cf11`  
		Last Modified: Wed, 05 Feb 2025 01:10:44 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c05823ce56f2ee7ebe0155425a6cfcd238645db8549348a3229bf95d97ad7f6`  
		Last Modified: Wed, 05 Feb 2025 08:24:12 GMT  
		Size: 60.4 MB (60377794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc459b6f586268e69f383b27d9289655fa5f9b8d78cc50bbd5c46be1abb72b3`  
		Last Modified: Wed, 05 Feb 2025 08:21:21 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31` - unknown; unknown

```console
$ docker pull telegraf@sha256:7f6282c5ee6dde93f907ed498ddc21241d95227c6e88d4e986cfc530d156a1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6430643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d762ec04a44ad35905caa78088eb1345872cb5dfb2a0f115a4d0598427864bb`

```dockerfile
```

-	Layers:
	-	`sha256:bef5929ba977032fb78087fb87f0110831de2c9aece8fc9c0008328fb02e7e98`  
		Last Modified: Tue, 04 Feb 2025 22:39:31 GMT  
		Size: 6.4 MB (6416063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9410949d161794c0b3599abdfe0ae1fe817ab0c5e4464f6ecd24b5aa9cfa94b`  
		Last Modified: Tue, 04 Feb 2025 22:39:30 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31-alpine`

```console
$ docker pull telegraf@sha256:bf274ea9fbf49a62ed19478ea0badb0f040ee9db09725a94175fa5ffecd8b7ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:ba2879ac96fd18bebe4c194335b874fed284a3bcb26c1f976728d5c1917e2b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72155101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a170b8100d371adf3369933695bec97d426d1c68052e5f5ac7095c027d584b0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386a218cdb719a9576158ee1a7a44f91e4ca831aacaa99c77c4cc08a97a91d3a`  
		Last Modified: Fri, 14 Feb 2025 22:34:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b02cf70d3e15fbc1e627a366bd4ee04f1b87dbe5474dc9a33dac6af3e60913`  
		Last Modified: Fri, 14 Feb 2025 22:34:54 GMT  
		Size: 2.4 MB (2447985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52362ba785f3e9dfe7a835dee1206078f01677109c3321961083785dea5f380e`  
		Last Modified: Fri, 14 Feb 2025 22:34:57 GMT  
		Size: 66.1 MB (66079612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87823eebe559f47748506cb625ba45bf8ee21e45497482b145807fca62e0581`  
		Last Modified: Fri, 14 Feb 2025 22:34:55 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:561b5d3febe7ec49a6880f52c60a2e962e776f7d72e07eebbcf1795998814a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1084257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad041b757f4bde1051df284acc5642c2038bf93f83c50dfc4abb7394b82bd12e`

```dockerfile
```

-	Layers:
	-	`sha256:8ebe564a6114bab7156f964582817a92044c1b8b0e2f863a4e8cbd765438bf86`  
		Last Modified: Fri, 14 Feb 2025 22:10:18 GMT  
		Size: 1.1 MB (1069297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef8b23e8f8443f2c3d9bfc51273e7f15ea22ae1e25202b2be769cdfec542efa9`  
		Last Modified: Fri, 14 Feb 2025 22:10:18 GMT  
		Size: 15.0 KB (14960 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a1eee96d7b4b95b7a2482715cde7f5efffef624e8e6f3b493c4c7e1eaba38615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66797318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0ae86f166140f943f2e6470e5c7a00960ffee837b0747f31248e30a071d09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a5f488a07a5f9b377e1e8af47680d864b0a298fd6acfe930441fecb3ecf84`  
		Last Modified: Sat, 15 Feb 2025 03:20:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a777ce7d187cf232aae59fd07445827d4a146c69dd2ff0adb80ede2329896`  
		Last Modified: Sat, 15 Feb 2025 10:11:16 GMT  
		Size: 2.5 MB (2533889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9ab4ab3455972429abe5f16a52674c53b992437c904a1c16a75642e09aa089`  
		Last Modified: Sat, 15 Feb 2025 06:30:26 GMT  
		Size: 60.2 MB (60171658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c14aabdf5557104adea5cdd7a2d77cea7e032d61a3cc12d11c6c65c3dc2b6`  
		Last Modified: Sat, 15 Feb 2025 06:30:24 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9f18e6537bdfe5df0c24f59d2f397a224f2f2f525b91c0c8e72adb9ebbb8465c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1080802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ddc32d0be2006d802595fdcd620b167bedf1af82ee142557f25ab9cd6f139e`

```dockerfile
```

-	Layers:
	-	`sha256:0ff35a494c1c5958a815f9e1e9b468fd4246630f76ccaa6c412c62af92d7a192`  
		Last Modified: Sat, 15 Feb 2025 10:10:19 GMT  
		Size: 1.1 MB (1065731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:105383f7c1f88fb4340b53e6324cd3c18bd5b55146d306b8c63f5734df3d8835`  
		Last Modified: Sat, 15 Feb 2025 10:10:19 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3`

```console
$ docker pull telegraf@sha256:c07851474ac4edd079b45750eca3ee6b8954d81736e4d0f5e88018ec56bb069d
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
$ docker pull telegraf@sha256:924a1e8c991087a7ce52a90dfba715c641be38aa497704068707089c6bbba63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157773984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b611451ad13075398bc84f6ee6a28d02583caa13add72a46549a3610f599f218`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.31.3
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 10 Jan 2025 18:06:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 07:11:25 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10a5068bceb1e490674294d0059f3244a8eb6ce7cc94ee00b6564c73147703f`  
		Last Modified: Tue, 04 Feb 2025 07:21:06 GMT  
		Size: 18.9 MB (18948067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b5b447d955db8b7069bc72e6eb4886061a3c646fc910e3da29e1a50ca8b7de`  
		Last Modified: Tue, 04 Feb 2025 09:54:18 GMT  
		Size: 1.8 KB (1778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767cb8b5780ab5a12365e16b784f2b42c75f2db2725aae23c91554819f0341c5`  
		Last Modified: Tue, 04 Feb 2025 12:19:25 GMT  
		Size: 66.3 MB (66285474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710675496ca2e9c84025424670bf8a459ef847a51ec79f4ad40138600647ec9e`  
		Last Modified: Tue, 04 Feb 2025 08:05:34 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:110a7e29d8ab83ee6eb40c178ce57aee08006ed950e87c6726342450b3b86782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6429049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78805e014ac908aaf4d1f741af03d90688d1a61659b85c245606c04b0c7e1f36`

```dockerfile
```

-	Layers:
	-	`sha256:687173db0c71b7075eb4eebc7203842999143979f1956940dcd8af6a480eedf4`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 6.4 MB (6414580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ad2a991c3f0cda7bdd268c33e265acd9b8ba7ce8347743f4462b328d9c866ad`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:80bf9a6198cdddd3e341bb1d843b04d263bcd1c39d3ebe8b2fd4348671a65598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145544334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ecf0158ea08df57a4b96312128c56f68db6f9d82ae9f446054f86bbcf0b80b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.31.3
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 10 Jan 2025 18:06:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 05:02:17 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 23:37:50 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d37da5ea34f101d528e16df8870c72e9bd46b0b2a815871f8b2cad7f226a6`  
		Last Modified: Tue, 04 Feb 2025 22:12:18 GMT  
		Size: 17.7 MB (17725432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7eff7fe833c3fbd6d3c6ddd5c4675fe3df5730fd39b06790f9bf9180f68be3`  
		Last Modified: Tue, 04 Feb 2025 23:37:47 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6e79ba0bf8c0c7e2cec56f584f900184f5281a417f6fe872a33864e846e3e8`  
		Last Modified: Mon, 10 Feb 2025 22:51:19 GMT  
		Size: 61.7 MB (61672360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c309b3a1ce3a10fa77348b583e640083dedac36625f96116e074ff34a55644cf`  
		Last Modified: Mon, 10 Feb 2025 22:51:11 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:60c769fdd167e9ad1a361c0e433ebd9430ae5b3ba1fcbc011ef1b089694bc18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2bcc9ce0c93896239fdf9c842b6754dcc946e4eaddacfdf6fba32ea89c7d09`

```dockerfile
```

-	Layers:
	-	`sha256:d5b7a63d54c86b99c07cd11af6d6be02cecd8da3ac90e710e6ec39a4503f448e`  
		Last Modified: Tue, 04 Feb 2025 18:30:30 GMT  
		Size: 6.4 MB (6409984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c1bf88c1303dab963aa25f03aa55530abbf185f9914e6df4f1c3f3e12cab9f5`  
		Last Modified: Tue, 04 Feb 2025 18:30:29 GMT  
		Size: 14.6 KB (14555 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:c746494a8535bfb5dc3bb0005eaa4614e6e1b34379f816a621d95b180958ea2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151155923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403e5a232c73416761ffa300da62f59822199e0af4a1749d6f059923e0b17105`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.31.3
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 10 Jan 2025 18:06:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Wed, 05 Feb 2025 00:14:09 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381030a63d0196bc211f3d91ddb8a25d6e1e4a40d13d2d068d59ee1acc77fe02`  
		Last Modified: Tue, 04 Feb 2025 23:38:16 GMT  
		Size: 18.9 MB (18870740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5c3c63ca133a2a6f025a1cac4edbb065fe2fa04d4cac68f1f4d1aaa01cf11`  
		Last Modified: Wed, 05 Feb 2025 01:10:44 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c05823ce56f2ee7ebe0155425a6cfcd238645db8549348a3229bf95d97ad7f6`  
		Last Modified: Wed, 05 Feb 2025 08:24:12 GMT  
		Size: 60.4 MB (60377794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc459b6f586268e69f383b27d9289655fa5f9b8d78cc50bbd5c46be1abb72b3`  
		Last Modified: Wed, 05 Feb 2025 08:21:21 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:7f6282c5ee6dde93f907ed498ddc21241d95227c6e88d4e986cfc530d156a1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6430643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d762ec04a44ad35905caa78088eb1345872cb5dfb2a0f115a4d0598427864bb`

```dockerfile
```

-	Layers:
	-	`sha256:bef5929ba977032fb78087fb87f0110831de2c9aece8fc9c0008328fb02e7e98`  
		Last Modified: Tue, 04 Feb 2025 22:39:31 GMT  
		Size: 6.4 MB (6416063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9410949d161794c0b3599abdfe0ae1fe817ab0c5e4464f6ecd24b5aa9cfa94b`  
		Last Modified: Tue, 04 Feb 2025 22:39:30 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.31.3-alpine`

```console
$ docker pull telegraf@sha256:bf274ea9fbf49a62ed19478ea0badb0f040ee9db09725a94175fa5ffecd8b7ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.31.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:ba2879ac96fd18bebe4c194335b874fed284a3bcb26c1f976728d5c1917e2b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72155101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a170b8100d371adf3369933695bec97d426d1c68052e5f5ac7095c027d584b0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386a218cdb719a9576158ee1a7a44f91e4ca831aacaa99c77c4cc08a97a91d3a`  
		Last Modified: Fri, 14 Feb 2025 22:34:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b02cf70d3e15fbc1e627a366bd4ee04f1b87dbe5474dc9a33dac6af3e60913`  
		Last Modified: Fri, 14 Feb 2025 22:34:54 GMT  
		Size: 2.4 MB (2447985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52362ba785f3e9dfe7a835dee1206078f01677109c3321961083785dea5f380e`  
		Last Modified: Fri, 14 Feb 2025 22:34:57 GMT  
		Size: 66.1 MB (66079612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87823eebe559f47748506cb625ba45bf8ee21e45497482b145807fca62e0581`  
		Last Modified: Fri, 14 Feb 2025 22:34:55 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:561b5d3febe7ec49a6880f52c60a2e962e776f7d72e07eebbcf1795998814a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1084257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad041b757f4bde1051df284acc5642c2038bf93f83c50dfc4abb7394b82bd12e`

```dockerfile
```

-	Layers:
	-	`sha256:8ebe564a6114bab7156f964582817a92044c1b8b0e2f863a4e8cbd765438bf86`  
		Last Modified: Fri, 14 Feb 2025 22:10:18 GMT  
		Size: 1.1 MB (1069297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef8b23e8f8443f2c3d9bfc51273e7f15ea22ae1e25202b2be769cdfec542efa9`  
		Last Modified: Fri, 14 Feb 2025 22:10:18 GMT  
		Size: 15.0 KB (14960 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.31.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a1eee96d7b4b95b7a2482715cde7f5efffef624e8e6f3b493c4c7e1eaba38615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66797318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0ae86f166140f943f2e6470e5c7a00960ffee837b0747f31248e30a071d09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.31.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a5f488a07a5f9b377e1e8af47680d864b0a298fd6acfe930441fecb3ecf84`  
		Last Modified: Sat, 15 Feb 2025 03:20:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a777ce7d187cf232aae59fd07445827d4a146c69dd2ff0adb80ede2329896`  
		Last Modified: Sat, 15 Feb 2025 10:11:16 GMT  
		Size: 2.5 MB (2533889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9ab4ab3455972429abe5f16a52674c53b992437c904a1c16a75642e09aa089`  
		Last Modified: Sat, 15 Feb 2025 06:30:26 GMT  
		Size: 60.2 MB (60171658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c14aabdf5557104adea5cdd7a2d77cea7e032d61a3cc12d11c6c65c3dc2b6`  
		Last Modified: Sat, 15 Feb 2025 06:30:24 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.31.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9f18e6537bdfe5df0c24f59d2f397a224f2f2f525b91c0c8e72adb9ebbb8465c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1080802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ddc32d0be2006d802595fdcd620b167bedf1af82ee142557f25ab9cd6f139e`

```dockerfile
```

-	Layers:
	-	`sha256:0ff35a494c1c5958a815f9e1e9b468fd4246630f76ccaa6c412c62af92d7a192`  
		Last Modified: Sat, 15 Feb 2025 10:10:19 GMT  
		Size: 1.1 MB (1065731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:105383f7c1f88fb4340b53e6324cd3c18bd5b55146d306b8c63f5734df3d8835`  
		Last Modified: Sat, 15 Feb 2025 10:10:19 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32`

```console
$ docker pull telegraf@sha256:0d45a59cf8aa0d70ee38707590c390bf93e5675cafff5fc467bb3deaf1553e3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32` - linux; amd64

```console
$ docker pull telegraf@sha256:75f1418e04faf01fa6d7dbd9b55b842de8e2ade65648d9f443d03658a55b50c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161509487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c031d53a0fada0a1cc4f33dd3efa424e393f1884e1004c716f8eeb5aed98dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.32.3
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 10 Jan 2025 18:06:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 07:11:25 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceba401331aa9149694245253600a7bfab5a70c5c556da97a2021d7f8a28e3bd`  
		Last Modified: Tue, 04 Feb 2025 10:22:02 GMT  
		Size: 18.9 MB (18948002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5decffb468ed91d8f8870b545fce926b72362d2f678622380d9424093ec26d84`  
		Last Modified: Tue, 04 Feb 2025 07:28:50 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e99ce456fe9450ff623d5c7a0c5b2f5ed96e574eb1824855c27817c000a7ba`  
		Last Modified: Tue, 04 Feb 2025 08:41:31 GMT  
		Size: 70.0 MB (70021047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d179ecf026ec7fb6703d2769208884763647b780701d38d3ad6f8f4c4eaa12a2`  
		Last Modified: Tue, 04 Feb 2025 07:30:50 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:cb931a950acd532a6bfd6b10903cd92b43d811dfcb5b6667901e7ae4eb911561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2beb3da9acde7aba00aa33bb2191b5af2f3df9ecbd601182e26db648880f4fe0`

```dockerfile
```

-	Layers:
	-	`sha256:712b7b4a7e1118a31fe4d82e90d261b94f6ca5578cecfa1c3c50c7d207546863`  
		Last Modified: Fri, 07 Feb 2025 20:22:51 GMT  
		Size: 6.4 MB (6424038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63524b67f8041d55397f518e5af6c286f012f8df6974bbe0680117812b928f26`  
		Last Modified: Fri, 07 Feb 2025 20:22:49 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:4aa84f86799a612db75d3238a9fe03cf86ca334ac4bfecd47d7d4113edbb10cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148554837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de54822187119f8a56a513bdafd4c66a8f88e580de699da405f0e98f133d2d55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.32.3
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 10 Jan 2025 18:06:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 05:02:17 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 23:37:50 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d37da5ea34f101d528e16df8870c72e9bd46b0b2a815871f8b2cad7f226a6`  
		Last Modified: Tue, 04 Feb 2025 22:12:18 GMT  
		Size: 17.7 MB (17725432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7eff7fe833c3fbd6d3c6ddd5c4675fe3df5730fd39b06790f9bf9180f68be3`  
		Last Modified: Tue, 04 Feb 2025 23:37:47 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf70aefe3719702dbd94833da29fa795c128b685bea70616300426d56cb18f4`  
		Last Modified: Fri, 07 Feb 2025 20:22:53 GMT  
		Size: 64.7 MB (64682863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9e3b3c168fcca5e8fc731ec7c740b6f5a0fa7ee9f1fcb5904a4901eed55a3c`  
		Last Modified: Fri, 07 Feb 2025 20:22:50 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:6d1af87fc2809f5fe0a5c1610c5e6c8e4308d2cf7e2ae11544f397d587c37c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820e6ad1d63c5560122353558ae33228893101b690e76cf80d3ba43536646f62`

```dockerfile
```

-	Layers:
	-	`sha256:0b5d792333488891b03f0b784574869a10312353e0eb76f11967acd86eb8e20a`  
		Last Modified: Wed, 05 Feb 2025 08:35:49 GMT  
		Size: 6.4 MB (6419442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02091922e33ce14e5262a735256017abd5bf12ed099ce7c9bb931eed9529bdde`  
		Last Modified: Fri, 07 Feb 2025 20:22:48 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:dec027775cf352798a5e20df10406c7305f262938fb686ed2acd0ac192b71e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153929637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69762705fdb42a444a2e753a597fc6ffe93604e9e0a512a918e8c07f64995301`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.32.3
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 10 Jan 2025 18:06:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Wed, 05 Feb 2025 00:14:09 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381030a63d0196bc211f3d91ddb8a25d6e1e4a40d13d2d068d59ee1acc77fe02`  
		Last Modified: Tue, 04 Feb 2025 23:38:16 GMT  
		Size: 18.9 MB (18870740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5c3c63ca133a2a6f025a1cac4edbb065fe2fa04d4cac68f1f4d1aaa01cf11`  
		Last Modified: Wed, 05 Feb 2025 01:10:44 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d7df1c4835dc9f870fc440283ce93a64342aa82bf086f63d8db3df8b949a97`  
		Last Modified: Wed, 05 Feb 2025 16:25:53 GMT  
		Size: 63.2 MB (63151510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3cb9bff23703aff0f53aff90565012ee995efbb5cd8da166317734eaac6173`  
		Last Modified: Wed, 05 Feb 2025 16:25:49 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32` - unknown; unknown

```console
$ docker pull telegraf@sha256:d86347fa97b903d6cfc71f51257ec88df3fe5fe0d32209087a52dd0ae17d85ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6439294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68add4e0ec8801a8c1dc0e9ce42569af6a1670ae735af932bcf387937e0a705b`

```dockerfile
```

-	Layers:
	-	`sha256:88cc4eb5358f5f172183cfa3877bd91f15aac75a831d7f473686802a0dde807b`  
		Last Modified: Fri, 07 Feb 2025 20:22:53 GMT  
		Size: 6.4 MB (6424714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f41edcd37193654485b644736cfe6154baa9d9c13042365bdd677ff25b639bdc`  
		Last Modified: Tue, 04 Feb 2025 22:40:03 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32-alpine`

```console
$ docker pull telegraf@sha256:9613ea0126325721f7087013726dadd23bf0aff8caed38d9337c449cdb66f05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:3ad9fa3557eec07393d93ba99a10a803a1d358c08aee5b31f11927ed45248331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75899910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87127c7ae451c11d56da2e3bbdb0133e4fc5465199f4a064700dc7bc1b95f94d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb2f8452f18fa5ca6d6eab55873b03df9cb04ec2a5cbef0b0347252dd1f1b98`  
		Last Modified: Fri, 14 Feb 2025 22:10:30 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1849576e5bfb8707e5b6da1ed76fc1b4642590a5cd627cc954d4458c972b87`  
		Last Modified: Fri, 14 Feb 2025 22:10:31 GMT  
		Size: 2.4 MB (2447977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8976f17c93a72e5f006514ed0e2d593d5fa816d872152c28e428bea70d7a275`  
		Last Modified: Fri, 14 Feb 2025 22:13:09 GMT  
		Size: 69.8 MB (69824429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0c5ba34859540677e65faaa6f81da813c58e83b5870ad2c8611227ad0b1a0`  
		Last Modified: Fri, 14 Feb 2025 22:10:32 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6a788cf31b15ae6004a2eb7b8e1abe4b99d5f46318fabad2c75620283de0f097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1093716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9834368eb385832d1124281f968481309de1c0912c4bea4bad334e1ee56503`

```dockerfile
```

-	Layers:
	-	`sha256:36d17874c7c519d61791ce6538dcf5b70d8d316102b689fadc4fcbf715597e97`  
		Last Modified: Fri, 14 Feb 2025 22:10:24 GMT  
		Size: 1.1 MB (1078755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53875bd2d4d184394b04b7247846ef535add592138dcbbc0131261f51dd4b97`  
		Last Modified: Fri, 14 Feb 2025 22:10:24 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5c131e9d3dfd41b67fbe1efc79eade66effd3013805af278d26b9581ac0535eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69569876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7adaf8892bce40df4e537a256a91cdc51bfcdaf585b04cdc584cdded2e35ab2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a5f488a07a5f9b377e1e8af47680d864b0a298fd6acfe930441fecb3ecf84`  
		Last Modified: Sat, 15 Feb 2025 03:20:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a777ce7d187cf232aae59fd07445827d4a146c69dd2ff0adb80ede2329896`  
		Last Modified: Sat, 15 Feb 2025 10:11:16 GMT  
		Size: 2.5 MB (2533889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd034834e7dc25546d11a5edde9078270a777c1002a13613255b26db02298a6`  
		Last Modified: Sat, 15 Feb 2025 11:18:03 GMT  
		Size: 62.9 MB (62944215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d8419ba9fcec72ee59593f2912c265a2f2650c283c863e9e30235da563b5f`  
		Last Modified: Sat, 15 Feb 2025 11:18:00 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e951a2565274dbce09494aac2324db6c6f4fe6b0940ca7528fc4c98c8023c85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33f51f8d0f3468d4c73164109a47998bc26ee6bb0739487e7e5c768a16499b1`

```dockerfile
```

-	Layers:
	-	`sha256:bb8efb89840ee2ef6a38b956f3d6cbdbf3e368f97c83314121ef06c9cc5b3a98`  
		Last Modified: Sat, 15 Feb 2025 10:10:24 GMT  
		Size: 1.1 MB (1074382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c6663ca7744f97d48d6c22ad8f29c6a45701e956bceefa937ea8e5eeab84f7b`  
		Last Modified: Sat, 15 Feb 2025 10:10:24 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32.3`

```console
$ docker pull telegraf@sha256:0d45a59cf8aa0d70ee38707590c390bf93e5675cafff5fc467bb3deaf1553e3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32.3` - linux; amd64

```console
$ docker pull telegraf@sha256:75f1418e04faf01fa6d7dbd9b55b842de8e2ade65648d9f443d03658a55b50c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161509487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c031d53a0fada0a1cc4f33dd3efa424e393f1884e1004c716f8eeb5aed98dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.32.3
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 10 Jan 2025 18:06:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 07:11:25 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceba401331aa9149694245253600a7bfab5a70c5c556da97a2021d7f8a28e3bd`  
		Last Modified: Tue, 04 Feb 2025 10:22:02 GMT  
		Size: 18.9 MB (18948002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5decffb468ed91d8f8870b545fce926b72362d2f678622380d9424093ec26d84`  
		Last Modified: Tue, 04 Feb 2025 07:28:50 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e99ce456fe9450ff623d5c7a0c5b2f5ed96e574eb1824855c27817c000a7ba`  
		Last Modified: Tue, 04 Feb 2025 08:41:31 GMT  
		Size: 70.0 MB (70021047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d179ecf026ec7fb6703d2769208884763647b780701d38d3ad6f8f4c4eaa12a2`  
		Last Modified: Tue, 04 Feb 2025 07:30:50 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:cb931a950acd532a6bfd6b10903cd92b43d811dfcb5b6667901e7ae4eb911561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2beb3da9acde7aba00aa33bb2191b5af2f3df9ecbd601182e26db648880f4fe0`

```dockerfile
```

-	Layers:
	-	`sha256:712b7b4a7e1118a31fe4d82e90d261b94f6ca5578cecfa1c3c50c7d207546863`  
		Last Modified: Fri, 07 Feb 2025 20:22:51 GMT  
		Size: 6.4 MB (6424038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63524b67f8041d55397f518e5af6c286f012f8df6974bbe0680117812b928f26`  
		Last Modified: Fri, 07 Feb 2025 20:22:49 GMT  
		Size: 14.5 KB (14470 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:4aa84f86799a612db75d3238a9fe03cf86ca334ac4bfecd47d7d4113edbb10cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148554837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de54822187119f8a56a513bdafd4c66a8f88e580de699da405f0e98f133d2d55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.32.3
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 10 Jan 2025 18:06:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 05:02:17 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 23:37:50 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d37da5ea34f101d528e16df8870c72e9bd46b0b2a815871f8b2cad7f226a6`  
		Last Modified: Tue, 04 Feb 2025 22:12:18 GMT  
		Size: 17.7 MB (17725432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7eff7fe833c3fbd6d3c6ddd5c4675fe3df5730fd39b06790f9bf9180f68be3`  
		Last Modified: Tue, 04 Feb 2025 23:37:47 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf70aefe3719702dbd94833da29fa795c128b685bea70616300426d56cb18f4`  
		Last Modified: Fri, 07 Feb 2025 20:22:53 GMT  
		Size: 64.7 MB (64682863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9e3b3c168fcca5e8fc731ec7c740b6f5a0fa7ee9f1fcb5904a4901eed55a3c`  
		Last Modified: Fri, 07 Feb 2025 20:22:50 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:6d1af87fc2809f5fe0a5c1610c5e6c8e4308d2cf7e2ae11544f397d587c37c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820e6ad1d63c5560122353558ae33228893101b690e76cf80d3ba43536646f62`

```dockerfile
```

-	Layers:
	-	`sha256:0b5d792333488891b03f0b784574869a10312353e0eb76f11967acd86eb8e20a`  
		Last Modified: Wed, 05 Feb 2025 08:35:49 GMT  
		Size: 6.4 MB (6419442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02091922e33ce14e5262a735256017abd5bf12ed099ce7c9bb931eed9529bdde`  
		Last Modified: Fri, 07 Feb 2025 20:22:48 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:dec027775cf352798a5e20df10406c7305f262938fb686ed2acd0ac192b71e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153929637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69762705fdb42a444a2e753a597fc6ffe93604e9e0a512a918e8c07f64995301`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENV TELEGRAF_VERSION=1.32.3
# Fri, 10 Jan 2025 18:06:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Fri, 10 Jan 2025 18:06:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 10 Jan 2025 18:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jan 2025 18:06:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Wed, 05 Feb 2025 00:14:09 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381030a63d0196bc211f3d91ddb8a25d6e1e4a40d13d2d068d59ee1acc77fe02`  
		Last Modified: Tue, 04 Feb 2025 23:38:16 GMT  
		Size: 18.9 MB (18870740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5c3c63ca133a2a6f025a1cac4edbb065fe2fa04d4cac68f1f4d1aaa01cf11`  
		Last Modified: Wed, 05 Feb 2025 01:10:44 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d7df1c4835dc9f870fc440283ce93a64342aa82bf086f63d8db3df8b949a97`  
		Last Modified: Wed, 05 Feb 2025 16:25:53 GMT  
		Size: 63.2 MB (63151510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3cb9bff23703aff0f53aff90565012ee995efbb5cd8da166317734eaac6173`  
		Last Modified: Wed, 05 Feb 2025 16:25:49 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:d86347fa97b903d6cfc71f51257ec88df3fe5fe0d32209087a52dd0ae17d85ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6439294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68add4e0ec8801a8c1dc0e9ce42569af6a1670ae735af932bcf387937e0a705b`

```dockerfile
```

-	Layers:
	-	`sha256:88cc4eb5358f5f172183cfa3877bd91f15aac75a831d7f473686802a0dde807b`  
		Last Modified: Fri, 07 Feb 2025 20:22:53 GMT  
		Size: 6.4 MB (6424714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f41edcd37193654485b644736cfe6154baa9d9c13042365bdd677ff25b639bdc`  
		Last Modified: Tue, 04 Feb 2025 22:40:03 GMT  
		Size: 14.6 KB (14580 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.32.3-alpine`

```console
$ docker pull telegraf@sha256:9613ea0126325721f7087013726dadd23bf0aff8caed38d9337c449cdb66f05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.32.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:3ad9fa3557eec07393d93ba99a10a803a1d358c08aee5b31f11927ed45248331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75899910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87127c7ae451c11d56da2e3bbdb0133e4fc5465199f4a064700dc7bc1b95f94d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb2f8452f18fa5ca6d6eab55873b03df9cb04ec2a5cbef0b0347252dd1f1b98`  
		Last Modified: Fri, 14 Feb 2025 22:10:30 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1849576e5bfb8707e5b6da1ed76fc1b4642590a5cd627cc954d4458c972b87`  
		Last Modified: Fri, 14 Feb 2025 22:10:31 GMT  
		Size: 2.4 MB (2447977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8976f17c93a72e5f006514ed0e2d593d5fa816d872152c28e428bea70d7a275`  
		Last Modified: Fri, 14 Feb 2025 22:13:09 GMT  
		Size: 69.8 MB (69824429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a0c5ba34859540677e65faaa6f81da813c58e83b5870ad2c8611227ad0b1a0`  
		Last Modified: Fri, 14 Feb 2025 22:10:32 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6a788cf31b15ae6004a2eb7b8e1abe4b99d5f46318fabad2c75620283de0f097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1093716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9834368eb385832d1124281f968481309de1c0912c4bea4bad334e1ee56503`

```dockerfile
```

-	Layers:
	-	`sha256:36d17874c7c519d61791ce6538dcf5b70d8d316102b689fadc4fcbf715597e97`  
		Last Modified: Fri, 14 Feb 2025 22:10:24 GMT  
		Size: 1.1 MB (1078755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53875bd2d4d184394b04b7247846ef535add592138dcbbc0131261f51dd4b97`  
		Last Modified: Fri, 14 Feb 2025 22:10:24 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.32.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5c131e9d3dfd41b67fbe1efc79eade66effd3013805af278d26b9581ac0535eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69569876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7adaf8892bce40df4e537a256a91cdc51bfcdaf585b04cdc584cdded2e35ab2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a5f488a07a5f9b377e1e8af47680d864b0a298fd6acfe930441fecb3ecf84`  
		Last Modified: Sat, 15 Feb 2025 03:20:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a777ce7d187cf232aae59fd07445827d4a146c69dd2ff0adb80ede2329896`  
		Last Modified: Sat, 15 Feb 2025 10:11:16 GMT  
		Size: 2.5 MB (2533889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd034834e7dc25546d11a5edde9078270a777c1002a13613255b26db02298a6`  
		Last Modified: Sat, 15 Feb 2025 11:18:03 GMT  
		Size: 62.9 MB (62944215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d8419ba9fcec72ee59593f2912c265a2f2650c283c863e9e30235da563b5f`  
		Last Modified: Sat, 15 Feb 2025 11:18:00 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.32.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e951a2565274dbce09494aac2324db6c6f4fe6b0940ca7528fc4c98c8023c85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33f51f8d0f3468d4c73164109a47998bc26ee6bb0739487e7e5c768a16499b1`

```dockerfile
```

-	Layers:
	-	`sha256:bb8efb89840ee2ef6a38b956f3d6cbdbf3e368f97c83314121ef06c9cc5b3a98`  
		Last Modified: Sat, 15 Feb 2025 10:10:24 GMT  
		Size: 1.1 MB (1074382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c6663ca7744f97d48d6c22ad8f29c6a45701e956bceefa937ea8e5eeab84f7b`  
		Last Modified: Sat, 15 Feb 2025 10:10:24 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33`

```console
$ docker pull telegraf@sha256:6f504d712bd1d89795d9ea1c3ba99fbde9940bb0ff9283dae66ce968c7918c8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33` - linux; amd64

```console
$ docker pull telegraf@sha256:24660309ba3a1c66bfc3a448cb19a95e7518dd79e1628f4f3a21c105dde168fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167822361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078a180e8972114bdf811c7697cb6a50a3e3d6dba8f28935ecbc0f5acb1c73a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 07:11:25 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d4e0873912c055077ef4f89ecfd8260f24755683b1c2938f81d43dae8d0a0b`  
		Last Modified: Tue, 11 Feb 2025 04:00:15 GMT  
		Size: 18.9 MB (18948066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e21bc83d55ce2eae8734507e32fb9b580a611fcd84616a5385431d84849077`  
		Last Modified: Tue, 11 Feb 2025 01:55:54 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141311c93e218f848ec55b344ecbf5dba33d21ebb5a04b8900e7d835c9661e49`  
		Last Modified: Tue, 11 Feb 2025 03:10:16 GMT  
		Size: 76.3 MB (76333860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a4656be874b72abbc9fe20e5b4e644519ac2e85b4042d658c38e1ed75ed0a6`  
		Last Modified: Tue, 11 Feb 2025 03:10:13 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:62e35d28130f777575cc4299d1c1377a753d361a9ce3a64b63201288ae354ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6453902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8748831b12eb3a02017b24f640cacabaf26a035b0642e6328ae1881f32970324`

```dockerfile
```

-	Layers:
	-	`sha256:7925933ebde796c104dac38aad11ad055aefc482fdfa962cf09399220f5a2ed5`  
		Last Modified: Tue, 11 Feb 2025 07:49:12 GMT  
		Size: 6.4 MB (6439130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a90de9775523f760a55bc74c579187cefcd855087268b66fbdfdb331230973b0`  
		Last Modified: Tue, 11 Feb 2025 05:08:35 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:631c670d815298bf1f01e9fc14a70a9c7bd7df381413c2f6f8cf9703f88c6acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154403882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b7d15c4334993a82be810f026fa39135482da26066349e5f69993fa3cb98a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 05:02:17 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 23:37:50 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d37da5ea34f101d528e16df8870c72e9bd46b0b2a815871f8b2cad7f226a6`  
		Last Modified: Tue, 04 Feb 2025 22:12:18 GMT  
		Size: 17.7 MB (17725432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7eff7fe833c3fbd6d3c6ddd5c4675fe3df5730fd39b06790f9bf9180f68be3`  
		Last Modified: Tue, 04 Feb 2025 23:37:47 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad85eae4eeefe28382b2b6ac022363abf12720aad417db847747f7cedc24e4f`  
		Last Modified: Tue, 11 Feb 2025 04:23:31 GMT  
		Size: 70.5 MB (70531910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf78465c33b061c5ae7946dbbaa605f1f867b1eb067fa2855063e286ac831242`  
		Last Modified: Tue, 11 Feb 2025 04:29:12 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:93190e99f59af7e4b86571b6be0b588840260f7a057d24c488ebe065c5db4eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6449408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87aed9440d4d8fa5f34ec0f4f034d2ada4b4415c95fce9276d64b5270762d6db`

```dockerfile
```

-	Layers:
	-	`sha256:bea2ca2705b89231972f0f25adccd1a433f3d0bfd15e8e4e3fd71d4068b5d196`  
		Last Modified: Tue, 11 Feb 2025 05:09:10 GMT  
		Size: 6.4 MB (6434542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2665fc8fe71fcacebb712ffb1f8fa69073fee2a894fa79dcd10281dff936e306`  
		Last Modified: Tue, 11 Feb 2025 05:25:06 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:bd8e98bd0021cedafc629f863a7a13816acca9d16f23f1eb1c4c2f54818728cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159822128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee0a4a1e197bbc31867b490330220717b83648d1f07f4283ecb9848c43a6c36`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Wed, 05 Feb 2025 00:14:09 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381030a63d0196bc211f3d91ddb8a25d6e1e4a40d13d2d068d59ee1acc77fe02`  
		Last Modified: Tue, 04 Feb 2025 23:38:16 GMT  
		Size: 18.9 MB (18870740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5c3c63ca133a2a6f025a1cac4edbb065fe2fa04d4cac68f1f4d1aaa01cf11`  
		Last Modified: Wed, 05 Feb 2025 01:10:44 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84cc46bea0acdbf38c9243168a033d827d80cfd85bb219b721edd95577fcc4a3`  
		Last Modified: Tue, 11 Feb 2025 01:33:17 GMT  
		Size: 69.0 MB (69043999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595a0bcd77a1de47648cb64e26e6093be1c42e75b98842317aa0d888468d5e88`  
		Last Modified: Tue, 11 Feb 2025 01:33:14 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33` - unknown; unknown

```console
$ docker pull telegraf@sha256:a884648d9760415806941d99d04c234379909ef09f178712622c76f22f29bf24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6454712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9aa4f05445d9887b1a75af39545bee1194897ae9e7e166ff94e0d115959be0`

```dockerfile
```

-	Layers:
	-	`sha256:04aee3a897d353de3b0addfa54bf5d0422e3f2f55ed48f93f8c9e837d872bef6`  
		Last Modified: Tue, 11 Feb 2025 05:08:58 GMT  
		Size: 6.4 MB (6439818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0cfcb447a7357c3183fa482ae05da069f9d94411dbc7cbfe2925683471fc795`  
		Last Modified: Tue, 11 Feb 2025 05:08:56 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33-alpine`

```console
$ docker pull telegraf@sha256:69fa36580c611f3035ab7925194cd62b53651cc0d7795219ce9345560ec29d77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e001ac229a01e097b80d6d23a6182691a7c1cad10869f684597ee609e33a6b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82201285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb39c98bfad6a37dc90ba4085099a0f6f9c513aae8bba47efbe7a3f442ae89d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c0bed9355d3eb54aa1208d3a20257a76f64080773dc86dcb02a82c6e8f82c6`  
		Last Modified: Fri, 14 Feb 2025 22:10:31 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325236e58b26876274c2856b683e82eaf5bdecf70373559cbcbe456230a5f053`  
		Last Modified: Fri, 14 Feb 2025 22:10:32 GMT  
		Size: 2.4 MB (2447975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6031a4ba8445bd07a336bf1dd87e8fc25a2b331379934204cd688e656b4a9a`  
		Last Modified: Fri, 14 Feb 2025 22:10:34 GMT  
		Size: 76.1 MB (76125805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8e7ad7c1c42825ed080658aaa640df496aa868c7efb879c706b8147cff5710`  
		Last Modified: Fri, 14 Feb 2025 22:10:33 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:16d454cb57b400e67295e59abd73a643329b519fce6d55bd24dfb96cecd5c9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1109110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a241722ce577a08c5d381c1f78d5c1ae86f867161c20c23e86808423352077`

```dockerfile
```

-	Layers:
	-	`sha256:ad0137f95a7afc49f37e4adc720387b76f20227bbe6621e5ca331fb943377567`  
		Last Modified: Fri, 14 Feb 2025 22:10:29 GMT  
		Size: 1.1 MB (1093847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1528d844dfa92117a2ea7bf3a4ca3e75062348016828dcd367bba63a3e5e5ca1`  
		Last Modified: Fri, 14 Feb 2025 22:10:29 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6a65d050e306d9717bcc023d72592dca9d57822fa5cd6d6df109ed7238a19b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75469195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85926df0ec4603baa1eeb2e3715a4f2d8cd29fd6277a4dfbb38e415734fc306e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a5f488a07a5f9b377e1e8af47680d864b0a298fd6acfe930441fecb3ecf84`  
		Last Modified: Sat, 15 Feb 2025 03:20:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a777ce7d187cf232aae59fd07445827d4a146c69dd2ff0adb80ede2329896`  
		Last Modified: Sat, 15 Feb 2025 10:11:16 GMT  
		Size: 2.5 MB (2533889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bf10fc8b7214ca8fef9f7bb41b2d0347463acd22e2fbceedb7a5e8b8e8e343`  
		Last Modified: Sat, 15 Feb 2025 10:11:20 GMT  
		Size: 68.8 MB (68843532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd185c393dc552246958fc560ea1cc609f26d253c54abd6599bd16f158f4f22`  
		Last Modified: Sat, 15 Feb 2025 10:11:17 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:22d9a2b1dd0ae592bf224ebe3d2a54de598ef6648a29a48cd1b3a5177a39526c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1104870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1272b930dbce6f617c202d1a5ae455db4b97a9bb21c3d063c046406fa09f81`

```dockerfile
```

-	Layers:
	-	`sha256:c69531efe7feb8f84aa571217dd572369b538232ce2942a97f0c8ef8c8008b18`  
		Last Modified: Sat, 15 Feb 2025 10:10:31 GMT  
		Size: 1.1 MB (1089486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a68ad0bcd8f5bb69ea8993a1c6674fdac750648cae385ff459a274cb622b9a`  
		Last Modified: Sat, 15 Feb 2025 10:10:31 GMT  
		Size: 15.4 KB (15384 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33.2`

```console
$ docker pull telegraf@sha256:6f504d712bd1d89795d9ea1c3ba99fbde9940bb0ff9283dae66ce968c7918c8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33.2` - linux; amd64

```console
$ docker pull telegraf@sha256:24660309ba3a1c66bfc3a448cb19a95e7518dd79e1628f4f3a21c105dde168fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167822361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078a180e8972114bdf811c7697cb6a50a3e3d6dba8f28935ecbc0f5acb1c73a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 07:11:25 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d4e0873912c055077ef4f89ecfd8260f24755683b1c2938f81d43dae8d0a0b`  
		Last Modified: Tue, 11 Feb 2025 04:00:15 GMT  
		Size: 18.9 MB (18948066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e21bc83d55ce2eae8734507e32fb9b580a611fcd84616a5385431d84849077`  
		Last Modified: Tue, 11 Feb 2025 01:55:54 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141311c93e218f848ec55b344ecbf5dba33d21ebb5a04b8900e7d835c9661e49`  
		Last Modified: Tue, 11 Feb 2025 03:10:16 GMT  
		Size: 76.3 MB (76333860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a4656be874b72abbc9fe20e5b4e644519ac2e85b4042d658c38e1ed75ed0a6`  
		Last Modified: Tue, 11 Feb 2025 03:10:13 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:62e35d28130f777575cc4299d1c1377a753d361a9ce3a64b63201288ae354ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6453902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8748831b12eb3a02017b24f640cacabaf26a035b0642e6328ae1881f32970324`

```dockerfile
```

-	Layers:
	-	`sha256:7925933ebde796c104dac38aad11ad055aefc482fdfa962cf09399220f5a2ed5`  
		Last Modified: Tue, 11 Feb 2025 07:49:12 GMT  
		Size: 6.4 MB (6439130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a90de9775523f760a55bc74c579187cefcd855087268b66fbdfdb331230973b0`  
		Last Modified: Tue, 11 Feb 2025 05:08:35 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.2` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:631c670d815298bf1f01e9fc14a70a9c7bd7df381413c2f6f8cf9703f88c6acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154403882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b7d15c4334993a82be810f026fa39135482da26066349e5f69993fa3cb98a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 05:02:17 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 23:37:50 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d37da5ea34f101d528e16df8870c72e9bd46b0b2a815871f8b2cad7f226a6`  
		Last Modified: Tue, 04 Feb 2025 22:12:18 GMT  
		Size: 17.7 MB (17725432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7eff7fe833c3fbd6d3c6ddd5c4675fe3df5730fd39b06790f9bf9180f68be3`  
		Last Modified: Tue, 04 Feb 2025 23:37:47 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad85eae4eeefe28382b2b6ac022363abf12720aad417db847747f7cedc24e4f`  
		Last Modified: Tue, 11 Feb 2025 04:23:31 GMT  
		Size: 70.5 MB (70531910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf78465c33b061c5ae7946dbbaa605f1f867b1eb067fa2855063e286ac831242`  
		Last Modified: Tue, 11 Feb 2025 04:29:12 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:93190e99f59af7e4b86571b6be0b588840260f7a057d24c488ebe065c5db4eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6449408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87aed9440d4d8fa5f34ec0f4f034d2ada4b4415c95fce9276d64b5270762d6db`

```dockerfile
```

-	Layers:
	-	`sha256:bea2ca2705b89231972f0f25adccd1a433f3d0bfd15e8e4e3fd71d4068b5d196`  
		Last Modified: Tue, 11 Feb 2025 05:09:10 GMT  
		Size: 6.4 MB (6434542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2665fc8fe71fcacebb712ffb1f8fa69073fee2a894fa79dcd10281dff936e306`  
		Last Modified: Tue, 11 Feb 2025 05:25:06 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.2` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:bd8e98bd0021cedafc629f863a7a13816acca9d16f23f1eb1c4c2f54818728cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159822128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee0a4a1e197bbc31867b490330220717b83648d1f07f4283ecb9848c43a6c36`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Wed, 05 Feb 2025 00:14:09 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381030a63d0196bc211f3d91ddb8a25d6e1e4a40d13d2d068d59ee1acc77fe02`  
		Last Modified: Tue, 04 Feb 2025 23:38:16 GMT  
		Size: 18.9 MB (18870740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5c3c63ca133a2a6f025a1cac4edbb065fe2fa04d4cac68f1f4d1aaa01cf11`  
		Last Modified: Wed, 05 Feb 2025 01:10:44 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84cc46bea0acdbf38c9243168a033d827d80cfd85bb219b721edd95577fcc4a3`  
		Last Modified: Tue, 11 Feb 2025 01:33:17 GMT  
		Size: 69.0 MB (69043999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595a0bcd77a1de47648cb64e26e6093be1c42e75b98842317aa0d888468d5e88`  
		Last Modified: Tue, 11 Feb 2025 01:33:14 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:a884648d9760415806941d99d04c234379909ef09f178712622c76f22f29bf24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6454712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9aa4f05445d9887b1a75af39545bee1194897ae9e7e166ff94e0d115959be0`

```dockerfile
```

-	Layers:
	-	`sha256:04aee3a897d353de3b0addfa54bf5d0422e3f2f55ed48f93f8c9e837d872bef6`  
		Last Modified: Tue, 11 Feb 2025 05:08:58 GMT  
		Size: 6.4 MB (6439818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0cfcb447a7357c3183fa482ae05da069f9d94411dbc7cbfe2925683471fc795`  
		Last Modified: Tue, 11 Feb 2025 05:08:56 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.33.2-alpine`

```console
$ docker pull telegraf@sha256:69fa36580c611f3035ab7925194cd62b53651cc0d7795219ce9345560ec29d77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.33.2-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e001ac229a01e097b80d6d23a6182691a7c1cad10869f684597ee609e33a6b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82201285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb39c98bfad6a37dc90ba4085099a0f6f9c513aae8bba47efbe7a3f442ae89d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c0bed9355d3eb54aa1208d3a20257a76f64080773dc86dcb02a82c6e8f82c6`  
		Last Modified: Fri, 14 Feb 2025 22:10:31 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325236e58b26876274c2856b683e82eaf5bdecf70373559cbcbe456230a5f053`  
		Last Modified: Fri, 14 Feb 2025 22:10:32 GMT  
		Size: 2.4 MB (2447975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6031a4ba8445bd07a336bf1dd87e8fc25a2b331379934204cd688e656b4a9a`  
		Last Modified: Fri, 14 Feb 2025 22:10:34 GMT  
		Size: 76.1 MB (76125805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8e7ad7c1c42825ed080658aaa640df496aa868c7efb879c706b8147cff5710`  
		Last Modified: Fri, 14 Feb 2025 22:10:33 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.2-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:16d454cb57b400e67295e59abd73a643329b519fce6d55bd24dfb96cecd5c9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1109110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a241722ce577a08c5d381c1f78d5c1ae86f867161c20c23e86808423352077`

```dockerfile
```

-	Layers:
	-	`sha256:ad0137f95a7afc49f37e4adc720387b76f20227bbe6621e5ca331fb943377567`  
		Last Modified: Fri, 14 Feb 2025 22:10:29 GMT  
		Size: 1.1 MB (1093847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1528d844dfa92117a2ea7bf3a4ca3e75062348016828dcd367bba63a3e5e5ca1`  
		Last Modified: Fri, 14 Feb 2025 22:10:29 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.33.2-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6a65d050e306d9717bcc023d72592dca9d57822fa5cd6d6df109ed7238a19b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75469195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85926df0ec4603baa1eeb2e3715a4f2d8cd29fd6277a4dfbb38e415734fc306e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a5f488a07a5f9b377e1e8af47680d864b0a298fd6acfe930441fecb3ecf84`  
		Last Modified: Sat, 15 Feb 2025 03:20:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a777ce7d187cf232aae59fd07445827d4a146c69dd2ff0adb80ede2329896`  
		Last Modified: Sat, 15 Feb 2025 10:11:16 GMT  
		Size: 2.5 MB (2533889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bf10fc8b7214ca8fef9f7bb41b2d0347463acd22e2fbceedb7a5e8b8e8e343`  
		Last Modified: Sat, 15 Feb 2025 10:11:20 GMT  
		Size: 68.8 MB (68843532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd185c393dc552246958fc560ea1cc609f26d253c54abd6599bd16f158f4f22`  
		Last Modified: Sat, 15 Feb 2025 10:11:17 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.33.2-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:22d9a2b1dd0ae592bf224ebe3d2a54de598ef6648a29a48cd1b3a5177a39526c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1104870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1272b930dbce6f617c202d1a5ae455db4b97a9bb21c3d063c046406fa09f81`

```dockerfile
```

-	Layers:
	-	`sha256:c69531efe7feb8f84aa571217dd572369b538232ce2942a97f0c8ef8c8008b18`  
		Last Modified: Sat, 15 Feb 2025 10:10:31 GMT  
		Size: 1.1 MB (1089486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a68ad0bcd8f5bb69ea8993a1c6674fdac750648cae385ff459a274cb622b9a`  
		Last Modified: Sat, 15 Feb 2025 10:10:31 GMT  
		Size: 15.4 KB (15384 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:69fa36580c611f3035ab7925194cd62b53651cc0d7795219ce9345560ec29d77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e001ac229a01e097b80d6d23a6182691a7c1cad10869f684597ee609e33a6b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82201285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb39c98bfad6a37dc90ba4085099a0f6f9c513aae8bba47efbe7a3f442ae89d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c0bed9355d3eb54aa1208d3a20257a76f64080773dc86dcb02a82c6e8f82c6`  
		Last Modified: Fri, 14 Feb 2025 22:10:31 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325236e58b26876274c2856b683e82eaf5bdecf70373559cbcbe456230a5f053`  
		Last Modified: Fri, 14 Feb 2025 22:10:32 GMT  
		Size: 2.4 MB (2447975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6031a4ba8445bd07a336bf1dd87e8fc25a2b331379934204cd688e656b4a9a`  
		Last Modified: Fri, 14 Feb 2025 22:10:34 GMT  
		Size: 76.1 MB (76125805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8e7ad7c1c42825ed080658aaa640df496aa868c7efb879c706b8147cff5710`  
		Last Modified: Fri, 14 Feb 2025 22:10:33 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:16d454cb57b400e67295e59abd73a643329b519fce6d55bd24dfb96cecd5c9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1109110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a241722ce577a08c5d381c1f78d5c1ae86f867161c20c23e86808423352077`

```dockerfile
```

-	Layers:
	-	`sha256:ad0137f95a7afc49f37e4adc720387b76f20227bbe6621e5ca331fb943377567`  
		Last Modified: Fri, 14 Feb 2025 22:10:29 GMT  
		Size: 1.1 MB (1093847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1528d844dfa92117a2ea7bf3a4ca3e75062348016828dcd367bba63a3e5e5ca1`  
		Last Modified: Fri, 14 Feb 2025 22:10:29 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6a65d050e306d9717bcc023d72592dca9d57822fa5cd6d6df109ed7238a19b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75469195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85926df0ec4603baa1eeb2e3715a4f2d8cd29fd6277a4dfbb38e415734fc306e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Feb 2025 22:49:00 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61a5f488a07a5f9b377e1e8af47680d864b0a298fd6acfe930441fecb3ecf84`  
		Last Modified: Sat, 15 Feb 2025 03:20:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a777ce7d187cf232aae59fd07445827d4a146c69dd2ff0adb80ede2329896`  
		Last Modified: Sat, 15 Feb 2025 10:11:16 GMT  
		Size: 2.5 MB (2533889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bf10fc8b7214ca8fef9f7bb41b2d0347463acd22e2fbceedb7a5e8b8e8e343`  
		Last Modified: Sat, 15 Feb 2025 10:11:20 GMT  
		Size: 68.8 MB (68843532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd185c393dc552246958fc560ea1cc609f26d253c54abd6599bd16f158f4f22`  
		Last Modified: Sat, 15 Feb 2025 10:11:17 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:22d9a2b1dd0ae592bf224ebe3d2a54de598ef6648a29a48cd1b3a5177a39526c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1104870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1272b930dbce6f617c202d1a5ae455db4b97a9bb21c3d063c046406fa09f81`

```dockerfile
```

-	Layers:
	-	`sha256:c69531efe7feb8f84aa571217dd572369b538232ce2942a97f0c8ef8c8008b18`  
		Last Modified: Sat, 15 Feb 2025 10:10:31 GMT  
		Size: 1.1 MB (1089486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a68ad0bcd8f5bb69ea8993a1c6674fdac750648cae385ff459a274cb622b9a`  
		Last Modified: Sat, 15 Feb 2025 10:10:31 GMT  
		Size: 15.4 KB (15384 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:6f504d712bd1d89795d9ea1c3ba99fbde9940bb0ff9283dae66ce968c7918c8c
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
$ docker pull telegraf@sha256:24660309ba3a1c66bfc3a448cb19a95e7518dd79e1628f4f3a21c105dde168fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167822361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078a180e8972114bdf811c7697cb6a50a3e3d6dba8f28935ecbc0f5acb1c73a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 07:11:25 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d4e0873912c055077ef4f89ecfd8260f24755683b1c2938f81d43dae8d0a0b`  
		Last Modified: Tue, 11 Feb 2025 04:00:15 GMT  
		Size: 18.9 MB (18948066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e21bc83d55ce2eae8734507e32fb9b580a611fcd84616a5385431d84849077`  
		Last Modified: Tue, 11 Feb 2025 01:55:54 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141311c93e218f848ec55b344ecbf5dba33d21ebb5a04b8900e7d835c9661e49`  
		Last Modified: Tue, 11 Feb 2025 03:10:16 GMT  
		Size: 76.3 MB (76333860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a4656be874b72abbc9fe20e5b4e644519ac2e85b4042d658c38e1ed75ed0a6`  
		Last Modified: Tue, 11 Feb 2025 03:10:13 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:62e35d28130f777575cc4299d1c1377a753d361a9ce3a64b63201288ae354ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6453902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8748831b12eb3a02017b24f640cacabaf26a035b0642e6328ae1881f32970324`

```dockerfile
```

-	Layers:
	-	`sha256:7925933ebde796c104dac38aad11ad055aefc482fdfa962cf09399220f5a2ed5`  
		Last Modified: Tue, 11 Feb 2025 07:49:12 GMT  
		Size: 6.4 MB (6439130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a90de9775523f760a55bc74c579187cefcd855087268b66fbdfdb331230973b0`  
		Last Modified: Tue, 11 Feb 2025 05:08:35 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:631c670d815298bf1f01e9fc14a70a9c7bd7df381413c2f6f8cf9703f88c6acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154403882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b7d15c4334993a82be810f026fa39135482da26066349e5f69993fa3cb98a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 05:02:17 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 23:37:50 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d37da5ea34f101d528e16df8870c72e9bd46b0b2a815871f8b2cad7f226a6`  
		Last Modified: Tue, 04 Feb 2025 22:12:18 GMT  
		Size: 17.7 MB (17725432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7eff7fe833c3fbd6d3c6ddd5c4675fe3df5730fd39b06790f9bf9180f68be3`  
		Last Modified: Tue, 04 Feb 2025 23:37:47 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad85eae4eeefe28382b2b6ac022363abf12720aad417db847747f7cedc24e4f`  
		Last Modified: Tue, 11 Feb 2025 04:23:31 GMT  
		Size: 70.5 MB (70531910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf78465c33b061c5ae7946dbbaa605f1f867b1eb067fa2855063e286ac831242`  
		Last Modified: Tue, 11 Feb 2025 04:29:12 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:93190e99f59af7e4b86571b6be0b588840260f7a057d24c488ebe065c5db4eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6449408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87aed9440d4d8fa5f34ec0f4f034d2ada4b4415c95fce9276d64b5270762d6db`

```dockerfile
```

-	Layers:
	-	`sha256:bea2ca2705b89231972f0f25adccd1a433f3d0bfd15e8e4e3fd71d4068b5d196`  
		Last Modified: Tue, 11 Feb 2025 05:09:10 GMT  
		Size: 6.4 MB (6434542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2665fc8fe71fcacebb712ffb1f8fa69073fee2a894fa79dcd10281dff936e306`  
		Last Modified: Tue, 11 Feb 2025 05:25:06 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:bd8e98bd0021cedafc629f863a7a13816acca9d16f23f1eb1c4c2f54818728cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159822128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee0a4a1e197bbc31867b490330220717b83648d1f07f4283ecb9848c43a6c36`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Wed, 05 Feb 2025 00:14:09 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381030a63d0196bc211f3d91ddb8a25d6e1e4a40d13d2d068d59ee1acc77fe02`  
		Last Modified: Tue, 04 Feb 2025 23:38:16 GMT  
		Size: 18.9 MB (18870740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e5c3c63ca133a2a6f025a1cac4edbb065fe2fa04d4cac68f1f4d1aaa01cf11`  
		Last Modified: Wed, 05 Feb 2025 01:10:44 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84cc46bea0acdbf38c9243168a033d827d80cfd85bb219b721edd95577fcc4a3`  
		Last Modified: Tue, 11 Feb 2025 01:33:17 GMT  
		Size: 69.0 MB (69043999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595a0bcd77a1de47648cb64e26e6093be1c42e75b98842317aa0d888468d5e88`  
		Last Modified: Tue, 11 Feb 2025 01:33:14 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:a884648d9760415806941d99d04c234379909ef09f178712622c76f22f29bf24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6454712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9aa4f05445d9887b1a75af39545bee1194897ae9e7e166ff94e0d115959be0`

```dockerfile
```

-	Layers:
	-	`sha256:04aee3a897d353de3b0addfa54bf5d0422e3f2f55ed48f93f8c9e837d872bef6`  
		Last Modified: Tue, 11 Feb 2025 05:08:58 GMT  
		Size: 6.4 MB (6439818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0cfcb447a7357c3183fa482ae05da069f9d94411dbc7cbfe2925683471fc795`  
		Last Modified: Tue, 11 Feb 2025 05:08:56 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
