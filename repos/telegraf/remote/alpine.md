## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:fdf6d4bcdcfad281ac758edc437c63f8269b76029a32577228e92276e5816dae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4b5bf7ee33971b587f6a56098b0a9dae5f433538e9b37fed00e380dda6771b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76465975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1158ceb0ee52558da6454d482326523f1d3a27a725f7649606f8786464192595`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.32.0
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8407248640ce51895daeb226fca47e0d9a489324a81cd5f7b29b3b3c858ea96`  
		Last Modified: Mon, 09 Sep 2024 21:00:51 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd456413a5ad81c1400225c0d58e2579dba79235bfe0e5be3f57d5ba75758e47`  
		Last Modified: Mon, 09 Sep 2024 21:00:51 GMT  
		Size: 2.4 MB (2444815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a4d1e24eb773b01d5bf5198476daa9da3e007efac326a4e0cd5e5b2e4f5e68`  
		Last Modified: Mon, 09 Sep 2024 21:00:53 GMT  
		Size: 70.4 MB (70396747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8662223dfa2a764e67ee8c53547c560fe46f82c85abfe6640b17bcacbd3bdd5f`  
		Last Modified: Mon, 09 Sep 2024 21:00:51 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:ce43df1cc0e45b4c4b4bb3c0ef2fc3f77bb38a18ffb48b08454e6e1e13774c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1089203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd59cb9fd39a2192d59fc30b317b541408ed82e0bcda8ebac7334cf82bd331fc`

```dockerfile
```

-	Layers:
	-	`sha256:a6cc0dfd496f8b51fbaf36e103bc5aeef5640e837bc3ecc19254e5dc6bd6280b`  
		Last Modified: Mon, 09 Sep 2024 21:00:51 GMT  
		Size: 1.1 MB (1074167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60f8df29aefc9a5cc62c9603f14a009df07208d6d1fbe234591b7be8123a66d6`  
		Last Modified: Mon, 09 Sep 2024 21:00:51 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:914be2639aa0528293e87d9a1c89521b7905b61ce05490ebf8ee06f19db00d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70064723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c452efd6c8109dea34cd886fc2f889130c7c09ea2c3bc1e7933990f91769caf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENV TELEGRAF_VERSION=1.32.0
# Mon, 09 Sep 2024 19:33:37 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Sep 2024 19:33:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Sep 2024 19:33:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Sep 2024 19:33:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4b70a44519145916f8803166c99c3ba52ea4bf109ad21b6d3e97aaa6f17a6`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db919974f422fe094695197712c3932f2f53b2941206fb854ced215414963d4e`  
		Last Modified: Sat, 07 Sep 2024 11:57:52 GMT  
		Size: 2.5 MB (2530619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ce795c4e61b36d98415cebcbe5ae217a9496aae4855bbdac71015f558f269`  
		Last Modified: Tue, 10 Sep 2024 02:53:26 GMT  
		Size: 63.4 MB (63445850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d975a327eb6969aeeadae546b8e0124f9f6188afda9328174f97ff8c8320e9`  
		Last Modified: Tue, 10 Sep 2024 02:53:23 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f97b4d7add54399904e669c2fe70978f48ce0aa3a4e637a0dd3da66268825798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1085168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b890cc6a9b66b7d8466df8cc5762b9fc42610dee02244681bee6c9d59ef30cb`

```dockerfile
```

-	Layers:
	-	`sha256:4af855bef43bba7766793187024c913cbd20e9e80becc1947b04811f3c6bcf5f`  
		Last Modified: Tue, 10 Sep 2024 02:53:24 GMT  
		Size: 1.1 MB (1069844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aced2b9a2b37dffba4ff1522bd3a9d2f4ed17da031b16267e646d868280c25a`  
		Last Modified: Tue, 10 Sep 2024 02:53:23 GMT  
		Size: 15.3 KB (15324 bytes)  
		MIME: application/vnd.in-toto+json
