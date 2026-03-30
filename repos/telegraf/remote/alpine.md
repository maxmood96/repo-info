## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:811335001118729cd2bdbcf0aaa88fae62102ab85745bf5f4a0ed60cba56de4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:15c787ed509753ff1c98af9c858bc4e79a8838e2f97f9da94808690f237954a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87671535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d74b6eeb9d11ffd3cf0526e2dfd611c3f1a047bee5ab27f89f68f30cce3a66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 20:22:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 30 Mar 2026 20:22:44 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:22:52 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:22:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:22:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f3ac74f06ef64597e0008d5b58e2d631cbc2a1c7c8d7827de7f6084ffd1384`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841b2cba4b94e9cabe8821efc5c269224dc910b9f66659d5a0118790408f9f64`  
		Last Modified: Mon, 30 Mar 2026 20:23:08 GMT  
		Size: 2.6 MB (2563409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22318848ab211de8fbcfbd33472f3c9a9f45e5bf40b3964fd587be331ef0cfff`  
		Last Modified: Mon, 30 Mar 2026 20:23:10 GMT  
		Size: 81.3 MB (81302351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f3b3d70a34cca73560581366bf1aa5a7a571294392984eb390146e1a80a300`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c45de09e7ba9157e9b403a2dd99453df7bee97206572dabc5092a953691be95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03720b29716f6c0b29dbdaaee3000ef67a64556f9a2281d4cac081d6d996656`

```dockerfile
```

-	Layers:
	-	`sha256:98f0364ff7dd919bdcd1b7b1403d67ffa52a2b0edc4c62886b0e5011b3d3fc09`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 1.2 MB (1161511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ee92bd2e1843be3aaa75cc44cd91b73eaba636edd0cc70546201ffdd09dd9d0`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 15.2 KB (15219 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:fb0afd49cd58018b245cea4961f220c244fc777aa1ca0753135afd7c1f59a630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79408705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc70a72097954c4dd9b3106a74912f37b0a24e864006c9d69d2d1dcbbde7e87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 20:23:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 30 Mar 2026 20:23:01 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:23:09 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:23:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:23:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929ce7d3c4f4050324790939845bf90248d29e90794fd46af445c1b82fa8e3ea`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2376aa1e3858066a43b2936816204d70c2b668fa25a029d43112bb6fde89fc0e`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 2.6 MB (2627416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572e1b4bba075fe67f8adfc96feb476ce9866df13a73405592fb7efc167a67a3`  
		Last Modified: Mon, 30 Mar 2026 20:23:25 GMT  
		Size: 72.6 MB (72640871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b84aaa694985c4eda65e869bf5da5464e1a8a2d08ceb445751e354912483b0`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:936b6b08489b822579b383270e0805734d6dfceff3312eb28064c847078d400e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97cf381f8dcb2b3c9f182fa9c1b572003933f561a664db9074cf1c6ae7afb654`

```dockerfile
```

-	Layers:
	-	`sha256:4a8a6a2dc5feb376c8b91acda685d81ccc02f798d46c259afc3890bbe6e1601d`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 1.2 MB (1157150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020ec74ea2d5779e6a975977b3f564113afe329c270a94159417df24fb421131`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json
