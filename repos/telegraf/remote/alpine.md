## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:bf87b4ee59b7414835c0e521f94b581e34944532aa5e3bfa9d14ce15b0186455
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:81694c382091482020e81ef7915b2c880064d2be39289aeeb08bea0d18135abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83867786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e80037183581d7eda2e1b5ea01dc84bf476b92bc2a72be1301dc653d41965c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENV TELEGRAF_VERSION=1.34.2
# Mon, 14 Apr 2025 17:23:46 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d636bcae97e1bcd8f2e05222fe2ed293ad4e3cf61fc945f8e3ee2e339687c7c8`  
		Last Modified: Mon, 14 Apr 2025 21:45:17 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5472d162d1d24a1511b151559cd2596a0447b7f5999ea131929a10576b621d64`  
		Last Modified: Mon, 14 Apr 2025 21:45:17 GMT  
		Size: 2.4 MB (2449507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37848268fcdb275aaa512abc718cff6603a0aa124c18d19c68310eb03c4517f`  
		Last Modified: Mon, 14 Apr 2025 21:45:18 GMT  
		Size: 77.8 MB (77790776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c43fcaea5f9ed98a4cdf870afd5d0d1c9b6d266591374f764cef4a91df748c3`  
		Last Modified: Mon, 14 Apr 2025 21:45:17 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e117cb2a9222eaac9ec9d08dbfdeb5a6194c6f3ab1b5b3ed4c05da31a3b5ce7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1112851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358b30f105278e400a2dc381b99d788b54651f2d9d59e32004befb0d288cce7d`

```dockerfile
```

-	Layers:
	-	`sha256:4b466318cb35d5afd75650438dd152b093d57425c3c1c8eb4fd29f243560e4b5`  
		Last Modified: Mon, 14 Apr 2025 21:45:17 GMT  
		Size: 1.1 MB (1097588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10629f5243df1d04d4506fff3cb2be199b9b3555ae80da1e0332d87d19f470b9`  
		Last Modified: Mon, 14 Apr 2025 21:45:17 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6e8da97c1ee51411a8edceb8a9875e09026b87fccb6b4cb784d5ca2262344c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76670094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0927d5f4c68ac11638b534b35c501d05ffdf5d9c553c9826f868bdd4cf064805`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENV TELEGRAF_VERSION=1.34.2
# Mon, 14 Apr 2025 17:23:46 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
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
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d5d995abdafd4a08c914e411233ba7edd1fd18c43edff36c7e7aeda4ed250e`  
		Last Modified: Mon, 14 Apr 2025 21:45:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601ae3ffdf2a162bb798b5d6cd90fe82d45f9806f51408017234d7b1e575a3a6`  
		Last Modified: Mon, 14 Apr 2025 21:45:24 GMT  
		Size: 2.5 MB (2535625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0ddb346a4a30c1c699ca70797d5030ab47b4bf27bc919a1a1aad8edfb15bee`  
		Last Modified: Mon, 14 Apr 2025 21:45:26 GMT  
		Size: 70.0 MB (70042697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bedfac84d629a52aaa04b5e98913b2927c261fa9950fe9d7fe5dd2721d8ca14`  
		Last Modified: Mon, 14 Apr 2025 21:45:24 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:1e7dd201f0d047341155a882081e8762f241a5c05d0353ad34ac76ae74646d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1108612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19936f71adaed0f2c1a0df5618755a7f9d2856a40f4ccb94369c8cbe86707a49`

```dockerfile
```

-	Layers:
	-	`sha256:4a74a116076baec51e748e51b41ae8f8ac50b9e9858f3231e657429923b7c239`  
		Last Modified: Mon, 14 Apr 2025 21:45:24 GMT  
		Size: 1.1 MB (1093227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a36918405b96e57ccfe4cd94c2aa931ecc960aaa003d8649cba9cc1eb84899df`  
		Last Modified: Mon, 14 Apr 2025 21:45:24 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json
