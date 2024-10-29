## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:faf74a3d0023e352482a8e233fc72dbe97731034d6b54a15054950edee0c794c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:0e60fcade2617904b5e9f30494bb555f0e951775484da3b40aa962787ef9ce0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76897556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93990211f2e788b4c772d05db15382f804ce1df98dda29b6ac05dd8b5d2d1937`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9537ee40d1986c9a0b088a96967c7d306020309d4cd1814b6b57d0533ff3fd`  
		Last Modified: Mon, 28 Oct 2024 23:09:37 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ec636db516f46a9d8d4aa5aab9355e0d7896897696db5ba83835e416a43e57`  
		Last Modified: Mon, 28 Oct 2024 23:09:37 GMT  
		Size: 2.4 MB (2444850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7dff8c190884085d20df8703bff65d58612b812fb74aac0dfab0d9ae7b91c8`  
		Last Modified: Mon, 28 Oct 2024 23:09:38 GMT  
		Size: 70.8 MB (70828296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d7f86b0b53f796310d9a729b13a82d6bdb81bacf59eda6fb277943ff1b6683`  
		Last Modified: Mon, 28 Oct 2024 23:09:37 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:55f8b2d5681e5c2f8b922bcc07e5fe59b38076b7a7cb3f2a46236bb26a90707c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1090108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3677b8a542c60d2090820b6f5f18b3f06c4fc253ec9e4b28ca59553c38dd49a9`

```dockerfile
```

-	Layers:
	-	`sha256:81fdccf8a807790f443f1f9d43a0b2a858d45a8882d3c7a5ff459110e00fffa6`  
		Last Modified: Mon, 28 Oct 2024 23:09:37 GMT  
		Size: 1.1 MB (1075038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0ea5b0639104bdb1e46c538e93643d9ea713323ca759ac8bdb4520f99d4d67a`  
		Last Modified: Mon, 28 Oct 2024 23:09:37 GMT  
		Size: 15.1 KB (15070 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0f4af9dd3ca6bfdddabd61c47059305abe0f1645ff9977f1bd0de3a9f47c942b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70488468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ceca611f32b0a30da8c368aeeae0181d294d1c7629c8194463bf4cd6966db3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENV TELEGRAF_VERSION=1.32.2
# Mon, 28 Oct 2024 22:11:39 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Oct 2024 22:11:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 22:11:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 22:11:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deeb5bb87a9b047197ab047408d669771534ddd651ad86d0935717add352c29`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bb72149297f282480386f5a2054f02adec456717b0d41bb49babd2406e9d30`  
		Last Modified: Tue, 29 Oct 2024 05:55:52 GMT  
		Size: 2.5 MB (2530665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349cb361d357d596b46784c3aab8b40d7ab6bfc11370bc32d2f2e64b3a58ef69`  
		Last Modified: Tue, 29 Oct 2024 05:55:54 GMT  
		Size: 63.9 MB (63869554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a75af9d87df5bcc37f4f812701eaa18c518ba096c99bc06ea03cb23ee23984`  
		Last Modified: Tue, 29 Oct 2024 05:55:51 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a691ba84006379addb1b6b4de87624f2d574940ada8dc39bab1b2e18034ab5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1085901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c107c6a220b7ebfae8f538cd0972359bd494d4bcf751e569bbcdc8960e36f1`

```dockerfile
```

-	Layers:
	-	`sha256:9b51a4795172302ff2e859eae9a7468cd4cee5ebf7388454e7cffc23cff9ad35`  
		Last Modified: Tue, 29 Oct 2024 05:55:52 GMT  
		Size: 1.1 MB (1070715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:801da592539f340a4c04f9e7aedfeff5221fb9540be7b04ecdc459ba7a786164`  
		Last Modified: Tue, 29 Oct 2024 05:55:51 GMT  
		Size: 15.2 KB (15186 bytes)  
		MIME: application/vnd.in-toto+json
