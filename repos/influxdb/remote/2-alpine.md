## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:c7a85ad1bb1d13ad0640cb6a3a0320eee0de833e0c793b3f8bae605429fa865b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:8fb72e9b1dd5df2d2ecb8201c3dac3d85fb4c0d217187b72ba5c290b4f941279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89833441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d489cf7c69589a3bedfde0adf613af40abc5c50bd65b85ede0de8a3b1ee53580`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78233a51c37b63a5d0dfb3f19da2586c9fa861b54e0bbf1b70a80875cadced1f`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28110b5bbbeab324abf5501db842f1dd0df6a19d379e92e2c42129c9c5e33a62`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 9.6 MB (9630577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2c38391b43cf30fc9494bfd7310fe25d02e2e2aad0e6bbd3a6a31a7c5732eb`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 5.8 MB (5820949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ed1d717a25ee5fa59dd9e2b100b9c78b33de4bf8ca7d7d39093ce59626db21`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55011f35b7dce11140b1343d9973f66e6cec2cac89f82766dc8f715eaceba84`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 47.6 MB (47621802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c907588fe177b5f2b5b48a0bddae0407e281ccd24ba410096a8230ad70e19cb4`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 23.1 MB (23128304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d9303dc18ddb862d68ecfcf31b63e0fe84a004741980c5f40b2fdf8f4be39e`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3aad3cb080baac2e2da3a4257353e8b81e841f4b6bf7ac26523da6c53bcec1`  
		Last Modified: Thu, 20 Jun 2024 20:56:07 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19689c0021345c8f777d5d28db1668d598acbd646cc6e8c3ad36b4e027bd1ad`  
		Last Modified: Thu, 20 Jun 2024 20:56:08 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:eada47181c572dd69f1ff41ec2fcd0244a5d591d999967c523496979ca7f1c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.1 KB (887126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e908161ef6f1ea7600cbab8224d15602ea617dec76211ced2613c8f3c1b71644`

```dockerfile
```

-	Layers:
	-	`sha256:e00f50a1837979e2f81dee93e8b402b0041824e1772e44d526a1d6097fe2518f`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 856.4 KB (856380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb977e34a5a17908ac79ef59d798fd7cc4639a728471e38b928fb3d49cd45694`  
		Last Modified: Thu, 20 Jun 2024 20:56:06 GMT  
		Size: 30.7 KB (30746 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:955d89f24208a13237ea6639a0890b561fcf7d7119afcd5fa7cfab0fa9371a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86694141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4491c4e6c5b904335a09ab7e7c6b6862bda2361f191a920f6b1984f5677ccf6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae98a4ae3c1de8e7a286da32ecdb0266e175d5486f8c5e4d3022d080d8f905`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857cb5878ee6488e66a81f881a4385ffdedbec093fdae7d9c74af42727097279`  
		Last Modified: Fri, 07 Jun 2024 02:47:37 GMT  
		Size: 9.8 MB (9751022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e77bb794bfbe4b734bb3d91387c7cd21c37dc6c525e0b3b155dd6bef8e309ac`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 5.5 MB (5463801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c232048582dbb7db8df170578d8006f2911c96c65be609605d5808879f2a3`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12164450e5dadb31e0bd6bdc329c602882e3d5027861418844e3a1fa839c87e1`  
		Last Modified: Fri, 07 Jun 2024 02:47:39 GMT  
		Size: 45.7 MB (45722064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76194063f90681845e47a0f5a93525560c461abe2129826986655e7059aae04`  
		Last Modified: Fri, 07 Jun 2024 02:47:38 GMT  
		Size: 21.7 MB (21662512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac2792e159fb9f449dd7e5aab8ce5bcb0bc2026702ac0c83651624e7e88e542`  
		Last Modified: Fri, 07 Jun 2024 02:47:38 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a068f2af32ff04a5eb45e03401b70a40dda67da2faa1f68dfc6747c7e93bce9`  
		Last Modified: Fri, 07 Jun 2024 02:47:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87cc165bbd0b298be6d8ccb4f67448a5ebad44329a78a0b28b23279f42e6c9d`  
		Last Modified: Fri, 07 Jun 2024 02:47:39 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:213ed7adb0be45bea4b98aac0018c8a45a76a164151628877db57153df552071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **886.8 KB (886830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8985b6e3aa764084cf7bf2b39913882da25927985fa66ad03cb787d5e7a976d8`

```dockerfile
```

-	Layers:
	-	`sha256:d733450f4dd915bbef9a06e90eafab35c4da25f374b2fd8c2bb9255efc75442b`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 855.8 KB (855783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee1536efec89cabe16e168ce3893962213f885c312bcb2961dbf707938cca86d`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json
