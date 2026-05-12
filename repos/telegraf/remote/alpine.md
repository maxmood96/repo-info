## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:49fc4b3e60115966979d653e76874bd960acdd27cd484a4a57813132e474d882
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c7bba96a83d3784fa69230bfa127df503fc8fb40ed96579d1577695a4ebc4049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89781668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bde7e8a9f0886477eb58d149d3fdb897576a1ff2880814cec5bb3e33a87fe23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:53:34 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:53:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:53:41 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:41 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 11 May 2026 23:53:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632464fc81a2417f86866f355eb404dd6fbaf95f23753e20e4aa1e267529287c`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2019e1df3daf5a5b4b76e4c51b0f6852dfe81b1860b80f3453f1e6834f8b07e7`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 2.6 MB (2615506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55706eb6bc48155a245fd2f96c71cb107f44fcccdd2aaa7c8a9010f4d9f3531e`  
		Last Modified: Mon, 11 May 2026 23:53:59 GMT  
		Size: 83.3 MB (83301076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18d0f774411b978b4a6dcff56ac3efb4fe752d82ff76811fa2d292168e096ee`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:6cfc1222edb07a0523e4a8b7d809b2cba473b87420ca92dfc9494a8e05a0249b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e4e891c501b04fc88f432dee4f0cbe8b1a2f9fbef27a8b59b5e1c8c857b410`

```dockerfile
```

-	Layers:
	-	`sha256:87172905ac106dc4e375b2ee186d37f6d4ae3e2e57f8397ed23b9df4a4af5ef3`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 1.2 MB (1159425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95634f1fdd7e204e3763697b4cc7367156ab43224e38e2c5541d394a304ed5f2`  
		Last Modified: Mon, 11 May 2026 23:53:57 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:19af6c4fafd30c79942ce50f05f02e295c12e5b03235cdae3524693152d2297d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81139701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb01df9de16a90f3948b5ece3e32033cdede92445b135f94ab92f92ba653a91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:53:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:53:38 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:53:44 GMT
ENV TELEGRAF_VERSION=1.38.4
# Mon, 11 May 2026 23:53:44 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 11 May 2026 23:53:44 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 11 May 2026 23:53:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:53:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:53:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516037cb512d171e8192c72d6cce6bcc6520c5c810cd1897a55fad977b22648e`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee16394386df16ff764f3efa01797c33a2433da101aef041fd08fc6005c2cdc6`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 2.7 MB (2663399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a626a22da7deea10123bbb5b91da01956fbd43220b4895c44a51c0f606eeb453`  
		Last Modified: Mon, 11 May 2026 23:54:00 GMT  
		Size: 74.3 MB (74275535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8a4a41e5ca652cb64623bdbe2d62a7093dc0f2b34d0959c77727c15e396aea`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:2e7bcc746fce8c8515152b4009e46d0ccb46de3da94f69c8801fcc984c8309b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1169756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6a3537a13a07028d6032f354fb67501d10d8219ccc35d65313195b862e73d3`

```dockerfile
```

-	Layers:
	-	`sha256:dac57cdea5ed6e2c983aac5dd06719625adb227c4b87bc662d57a13712de8dc0`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 1.2 MB (1154414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e77d863cf01a81facd30cb97595935291e5ad1ceb3762e95f7082ff1fd5252`  
		Last Modified: Mon, 11 May 2026 23:53:58 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json
