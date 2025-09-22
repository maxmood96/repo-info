## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:fc3d0dbda3db0580d896477f12103c93c187e925293ed5b78945a953d3bc50b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:f33b67d0350f23c711eafd72d5523bb257510297ddcde391ce3edcfee38a3658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10797939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a551e0818fc898460e568e5e923066df94a89447efbdac1331d2832af5c9250`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 12:53:23 GMT
ENV NATS_SERVER=2.12.0
# Mon, 22 Sep 2025 12:53:23 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='67051df32cd22ae830811ebb8574f431094e26a458fa7562e486b1cf37316915' ;;     armhf) natsArch='arm6'; sha256='23a20ef82d9437c159a38c68f6e463545aaa7085286d104398ae71f0153d4a51' ;;     armv7) natsArch='arm7'; sha256='82e0c757dff71c0593dc8ae45afadbf5bab5835b98134e9b2973750f9849ca6c' ;;     x86_64) natsArch='amd64'; sha256='42f233b3e883ff96e9fa9ba0882b958138534bc5dd6c4da7318e296afc0da909' ;;     x86) natsArch='386'; sha256='56eccfd5c4e9b3b31dae1bbe0c71b83cfb5a74f5990694dbc7557549df0f6c88' ;;     s390x) natsArch='s390x'; sha256='c1902cd6faf29babd917bbffe1b287747659249ca4eefd2d786b0502524782c3' ;;     ppc64le) natsArch='ppc64le'; sha256='2b7490b3b05392b69a8e55f8873a7be4663b03eecb0ca001ffcd97d1b3c91f8d' ;;     loong64) natsArch='loong64'; sha256='d632ed768d645c0e58b0ff52eec14ff2a51c5f8690639457d4a92747ee9edc32' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Sep 2025 12:53:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Sep 2025 12:53:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5765d8000e535c5c4aef8ff03a942628e19c441bb91f22a6d36b723e8132e2e6`  
		Last Modified: Mon, 22 Sep 2025 20:35:15 GMT  
		Size: 7.0 MB (6997279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad20d952e11e490bbb046b0bcb2d56888bcbec4c9d560eccad3aaddeb3e9d488`  
		Last Modified: Mon, 22 Sep 2025 20:35:14 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966519a4df7548b9d9ac74fcf8c3f9b42b2d3699f6148c019af8d3fb0c940f01`  
		Last Modified: Mon, 22 Sep 2025 20:35:14 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:9ad6e7fe2490be69bc2597ff16d846802cace27817a8f76ac72ef362fec84971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e7e3aa3d321f56b680599bc635022da020c4e160871e13737fb3e9ffea295e`

```dockerfile
```

-	Layers:
	-	`sha256:b569f51e53b9695e36cb91602af468cdba4a519f7ad95a893e4825d93eafd274`  
		Last Modified: Mon, 22 Sep 2025 20:56:45 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:f128931da7e0bdbc3cf573753cee9d066f74aae29238bf24388c64fc4682a426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10227396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcdbc1d796cf443c76dac068ec57ccb9c98e27aa43d49b7c813f592934d27df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 12:53:23 GMT
ENV NATS_SERVER=2.12.0
# Mon, 22 Sep 2025 12:53:23 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='67051df32cd22ae830811ebb8574f431094e26a458fa7562e486b1cf37316915' ;;     armhf) natsArch='arm6'; sha256='23a20ef82d9437c159a38c68f6e463545aaa7085286d104398ae71f0153d4a51' ;;     armv7) natsArch='arm7'; sha256='82e0c757dff71c0593dc8ae45afadbf5bab5835b98134e9b2973750f9849ca6c' ;;     x86_64) natsArch='amd64'; sha256='42f233b3e883ff96e9fa9ba0882b958138534bc5dd6c4da7318e296afc0da909' ;;     x86) natsArch='386'; sha256='56eccfd5c4e9b3b31dae1bbe0c71b83cfb5a74f5990694dbc7557549df0f6c88' ;;     s390x) natsArch='s390x'; sha256='c1902cd6faf29babd917bbffe1b287747659249ca4eefd2d786b0502524782c3' ;;     ppc64le) natsArch='ppc64le'; sha256='2b7490b3b05392b69a8e55f8873a7be4663b03eecb0ca001ffcd97d1b3c91f8d' ;;     loong64) natsArch='loong64'; sha256='d632ed768d645c0e58b0ff52eec14ff2a51c5f8690639457d4a92747ee9edc32' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Sep 2025 12:53:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Sep 2025 12:53:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14c1f3efecd199139c56fba9be5fecf065228786bc17c7d64aad0324f46402d`  
		Last Modified: Mon, 22 Sep 2025 20:35:13 GMT  
		Size: 6.7 MB (6725515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0ed5944fbec7edad1a06ca138b5233ab8c1c1bd1a213069bcb5719c86c577b`  
		Last Modified: Mon, 22 Sep 2025 20:35:07 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce85cba0b6fb7f8bf416c2b42920f9d9e73cf4d6b9d141eae2a3631f8341c6a`  
		Last Modified: Mon, 22 Sep 2025 20:35:02 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7992829a2bfc5ed26b92106780f3e07b6ff810ecb1da77982bd86f2bc63495af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc16390f9b336af5a04703b3aa69fb14ecb4ed5671307a6f3ac333e0af6bd389`

```dockerfile
```

-	Layers:
	-	`sha256:ea87226647cabd65ce630dc61d5e3aa243023113cc28fac47f27f589420194e7`  
		Last Modified: Mon, 22 Sep 2025 20:56:48 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:89f83e5dfe265fa68edb34915549ace875625dd053808d028c42ee6f79b48d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9933187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3bbee31536a5e64187936c7b970e4f291954114d1998bf2d8278808e9f0c0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 12:53:23 GMT
ENV NATS_SERVER=2.12.0
# Mon, 22 Sep 2025 12:53:23 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='67051df32cd22ae830811ebb8574f431094e26a458fa7562e486b1cf37316915' ;;     armhf) natsArch='arm6'; sha256='23a20ef82d9437c159a38c68f6e463545aaa7085286d104398ae71f0153d4a51' ;;     armv7) natsArch='arm7'; sha256='82e0c757dff71c0593dc8ae45afadbf5bab5835b98134e9b2973750f9849ca6c' ;;     x86_64) natsArch='amd64'; sha256='42f233b3e883ff96e9fa9ba0882b958138534bc5dd6c4da7318e296afc0da909' ;;     x86) natsArch='386'; sha256='56eccfd5c4e9b3b31dae1bbe0c71b83cfb5a74f5990694dbc7557549df0f6c88' ;;     s390x) natsArch='s390x'; sha256='c1902cd6faf29babd917bbffe1b287747659249ca4eefd2d786b0502524782c3' ;;     ppc64le) natsArch='ppc64le'; sha256='2b7490b3b05392b69a8e55f8873a7be4663b03eecb0ca001ffcd97d1b3c91f8d' ;;     loong64) natsArch='loong64'; sha256='d632ed768d645c0e58b0ff52eec14ff2a51c5f8690639457d4a92747ee9edc32' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Sep 2025 12:53:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Sep 2025 12:53:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415d0881793a7c59fe09d2db3b4458094f2c51e92811a0a5a4e250c72c543e23`  
		Last Modified: Mon, 22 Sep 2025 20:35:08 GMT  
		Size: 6.7 MB (6713179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3d3e8049a2df4acf2b337f3641c594454dc0e48e78d2097aa55e8018016b2a`  
		Last Modified: Mon, 22 Sep 2025 20:35:08 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ded13cb37dbc2e446928d50072f5fb84fe3483cd48e6c5e8769593c4d45a5a4`  
		Last Modified: Mon, 22 Sep 2025 20:35:08 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:bc4aa066872d47082e7492ec421c3eb9ddc1fba99ed87906e85b913cdbba6243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b71436cdd6fbec4feb5df45ffc5845b0d5ac7ee1fa30f20ffa28949f596f7b9`

```dockerfile
```

-	Layers:
	-	`sha256:a12096730f23e599bf6c4c6bb0160eabf6c94338c0d27f02d33c0f73e2b93940`  
		Last Modified: Mon, 22 Sep 2025 20:56:52 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:0f0734daa3fde71096a8bcd870f37e9dfc0db8fb47619121d918812705e87bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10549855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74477e89b604fb34eb8128a873e2fdf268b3fc4071a07d3277d1c3dbd06c876`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 12:53:23 GMT
ENV NATS_SERVER=2.12.0
# Mon, 22 Sep 2025 12:53:23 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='67051df32cd22ae830811ebb8574f431094e26a458fa7562e486b1cf37316915' ;;     armhf) natsArch='arm6'; sha256='23a20ef82d9437c159a38c68f6e463545aaa7085286d104398ae71f0153d4a51' ;;     armv7) natsArch='arm7'; sha256='82e0c757dff71c0593dc8ae45afadbf5bab5835b98134e9b2973750f9849ca6c' ;;     x86_64) natsArch='amd64'; sha256='42f233b3e883ff96e9fa9ba0882b958138534bc5dd6c4da7318e296afc0da909' ;;     x86) natsArch='386'; sha256='56eccfd5c4e9b3b31dae1bbe0c71b83cfb5a74f5990694dbc7557549df0f6c88' ;;     s390x) natsArch='s390x'; sha256='c1902cd6faf29babd917bbffe1b287747659249ca4eefd2d786b0502524782c3' ;;     ppc64le) natsArch='ppc64le'; sha256='2b7490b3b05392b69a8e55f8873a7be4663b03eecb0ca001ffcd97d1b3c91f8d' ;;     loong64) natsArch='loong64'; sha256='d632ed768d645c0e58b0ff52eec14ff2a51c5f8690639457d4a92747ee9edc32' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Sep 2025 12:53:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Sep 2025 12:53:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6065eaa5309fc5c303986cc8584ec4ceaa9cf9791274a801915abe6212c18be7`  
		Last Modified: Mon, 22 Sep 2025 20:35:12 GMT  
		Size: 6.4 MB (6418135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113594ca74345cb3e4ec6aa7b95d4351336a2d51ce871d1516278062514dbb78`  
		Last Modified: Mon, 22 Sep 2025 20:35:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a066de14aea580c153cc54017275058276453bb30754fed9f3b716863161f19a`  
		Last Modified: Mon, 22 Sep 2025 20:35:12 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:48d9803eb9c320e16b616ab1de4a3f20d7a537de667879918f3b7828975b6280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2127a900895c3d00aff812ce1095b9bed90284c6d4ddbd67a6db393acbeed509`

```dockerfile
```

-	Layers:
	-	`sha256:1b777e1029b0f101d6160d4e4a3999343c23825472bcbed945fefb12db632696`  
		Last Modified: Mon, 22 Sep 2025 20:56:55 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:330c1e0af8d37e016c299a67a72d4a4bf274ea7cdc2aa19ebf2abc140e354a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10195084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82391b8bbf316b21052a47ac99a821e8bd3a9280e71b91ee772717e4d37952a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 12:53:23 GMT
ENV NATS_SERVER=2.12.0
# Mon, 22 Sep 2025 12:53:23 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='67051df32cd22ae830811ebb8574f431094e26a458fa7562e486b1cf37316915' ;;     armhf) natsArch='arm6'; sha256='23a20ef82d9437c159a38c68f6e463545aaa7085286d104398ae71f0153d4a51' ;;     armv7) natsArch='arm7'; sha256='82e0c757dff71c0593dc8ae45afadbf5bab5835b98134e9b2973750f9849ca6c' ;;     x86_64) natsArch='amd64'; sha256='42f233b3e883ff96e9fa9ba0882b958138534bc5dd6c4da7318e296afc0da909' ;;     x86) natsArch='386'; sha256='56eccfd5c4e9b3b31dae1bbe0c71b83cfb5a74f5990694dbc7557549df0f6c88' ;;     s390x) natsArch='s390x'; sha256='c1902cd6faf29babd917bbffe1b287747659249ca4eefd2d786b0502524782c3' ;;     ppc64le) natsArch='ppc64le'; sha256='2b7490b3b05392b69a8e55f8873a7be4663b03eecb0ca001ffcd97d1b3c91f8d' ;;     loong64) natsArch='loong64'; sha256='d632ed768d645c0e58b0ff52eec14ff2a51c5f8690639457d4a92747ee9edc32' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Sep 2025 12:53:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Sep 2025 12:53:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53715feca00522eeeb904e688ba46f9f6a7ca9b6296a30b53624f44e87767c1a`  
		Last Modified: Mon, 22 Sep 2025 20:34:57 GMT  
		Size: 6.5 MB (6466999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca0a82da5e24e78bd841dae1c330ef27961eb20b67052d7a8b8860e691cce6a`  
		Last Modified: Mon, 22 Sep 2025 20:34:56 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34351d43aaa584a0095b23b56fec3e1974b355d04a8e914effab9b9be157378`  
		Last Modified: Mon, 22 Sep 2025 20:34:57 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:899deddacf3750575ff12afb9c0cfd7935fd7f9498ddcdd746b9ec32c1b9d8e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6f94be82b5be62fc466087ed7687bd8c4a19fc15cef7e202aaf9bcd626d502`

```dockerfile
```

-	Layers:
	-	`sha256:62cc13bd933e633a0e1599be27f10658d936f4363e25aab9f4807c81470c54ce`  
		Last Modified: Mon, 22 Sep 2025 20:56:58 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:583dc6023bd46b29da71524c0905d64ecaadfeabf6c56c658037b44fc81c1e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10484938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b886097b67112e71dc338f6cad861ccd6f23973b53c216d3d1e0e91637d6fff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 12:53:23 GMT
ENV NATS_SERVER=2.12.0
# Mon, 22 Sep 2025 12:53:23 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='67051df32cd22ae830811ebb8574f431094e26a458fa7562e486b1cf37316915' ;;     armhf) natsArch='arm6'; sha256='23a20ef82d9437c159a38c68f6e463545aaa7085286d104398ae71f0153d4a51' ;;     armv7) natsArch='arm7'; sha256='82e0c757dff71c0593dc8ae45afadbf5bab5835b98134e9b2973750f9849ca6c' ;;     x86_64) natsArch='amd64'; sha256='42f233b3e883ff96e9fa9ba0882b958138534bc5dd6c4da7318e296afc0da909' ;;     x86) natsArch='386'; sha256='56eccfd5c4e9b3b31dae1bbe0c71b83cfb5a74f5990694dbc7557549df0f6c88' ;;     s390x) natsArch='s390x'; sha256='c1902cd6faf29babd917bbffe1b287747659249ca4eefd2d786b0502524782c3' ;;     ppc64le) natsArch='ppc64le'; sha256='2b7490b3b05392b69a8e55f8873a7be4663b03eecb0ca001ffcd97d1b3c91f8d' ;;     loong64) natsArch='loong64'; sha256='d632ed768d645c0e58b0ff52eec14ff2a51c5f8690639457d4a92747ee9edc32' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Sep 2025 12:53:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Sep 2025 12:53:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68a38c35c25851432e548e4f6311468d5e8019abd9f074be9d4f0421dbcb030`  
		Last Modified: Mon, 22 Sep 2025 20:34:58 GMT  
		Size: 6.8 MB (6838998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2978644e153684bc482789a42dfd9b53faf1ee77e354dc186afcb4f800a8813`  
		Last Modified: Mon, 22 Sep 2025 20:34:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c405b5135b2f42101c52e11f5872bc2628d9242aa1a8932d7e713b584180f46`  
		Last Modified: Mon, 22 Sep 2025 20:34:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:409730408a05c6b7c29cd2d9b79e803353c9bbbff4464e04d6a50d2d386bf574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc3102ff081b3780f5a927ffd0058fa22ee80e5afb023c3e6fe8c2159d0698e`

```dockerfile
```

-	Layers:
	-	`sha256:3fef583e358f058c5506e42e759c5763fdf1c3edc3e284872bb1d4f0657a121b`  
		Last Modified: Mon, 22 Sep 2025 20:57:01 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json
