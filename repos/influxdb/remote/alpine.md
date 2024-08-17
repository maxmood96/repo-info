## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:84934b1007a518d779df42b1e58e6185f1f09a81a6593c6cd0c242fb9fb5c2f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:519e3ba63232f834471dd9c946b897bc7f5e664bdad62cd53729373b9719ca78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92011346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:020918370a410b09f132845051e1082d8b5a962d4dfd83f3225134c4b658eb67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14fef106b46a1d71a03840cac8ed7a447b41762df954efcba0338aca0344888`  
		Last Modified: Fri, 16 Aug 2024 21:57:57 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e5c984b26a7bc7540ae9329bf17bcbcfe97d671143232116347d782d7cb2f9`  
		Last Modified: Fri, 16 Aug 2024 21:57:58 GMT  
		Size: 9.6 MB (9640770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7667a95843eb9ca4aed84a70280597e16edf4bf1340f307144c1e12132023fa`  
		Last Modified: Fri, 16 Aug 2024 21:57:57 GMT  
		Size: 5.8 MB (5820952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f260790a0c12709a15fa1d4cc1fd7e7f0f776af845d2d861f00146fe59ba1543`  
		Last Modified: Fri, 16 Aug 2024 21:57:57 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0768ee5d1e2b635e816cb0f2e8054a984c36d1fb75ef67210e4fd4891511ba3f`  
		Last Modified: Fri, 16 Aug 2024 21:57:59 GMT  
		Size: 49.8 MB (49790468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f39b63cb5f666b39e3c2cce87a30d352228ff8593d95350f1ebf2c118ed7e6`  
		Last Modified: Fri, 16 Aug 2024 21:57:59 GMT  
		Size: 23.1 MB (23128297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a368c15ef24e0a4c4c8597fd8be2dd78c8d8d11ba17ee398708bcfa3b74ec25`  
		Last Modified: Fri, 16 Aug 2024 21:57:58 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d835ae914c5ed6c62bca5532b5d50b923a28c819cdbe1808c01872ecc6faa808`  
		Last Modified: Fri, 16 Aug 2024 21:57:59 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea1e32897bb1a01a225aebfbc6e092737abc10a983386321e54c93e3e0b2dc3`  
		Last Modified: Fri, 16 Aug 2024 21:57:59 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:1000c3307b83151b71dfbb966a81f389f8781cde1460b5294d11b851440fc505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545b7a6550b710a2ef8cf22e13451a28496ae042e4d763c5c454668b4eedd3f8`

```dockerfile
```

-	Layers:
	-	`sha256:ea2e09bc858d9377a0e5651780a8de70c17f91f6aa4e20eda91530920dd8cb56`  
		Last Modified: Fri, 16 Aug 2024 21:57:58 GMT  
		Size: 914.1 KB (914093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf504e5ea0652950f61cb3c154aaa840492e390121990804a959e7298262d51`  
		Last Modified: Fri, 16 Aug 2024 21:57:57 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c1a0ff5870f0e65b4b6ea68ffe095b0aae72d69f6762be3374ce46fe8449c6e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88694176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba58ea82eaa808f8f01411f9890a63419cb8b9fbd9e06b7d753882272b5c2067`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1de5eaf2a1972853375a025a0309628552446763159c73f9fb971eedad7e97c`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b42d817c706fa63528ebb9df4f22670ee67a5c112ac51b215bd8678ac9d67ad`  
		Last Modified: Fri, 26 Jul 2024 00:21:09 GMT  
		Size: 9.8 MB (9763425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b885d125af61f60c725f3f3ac857c0aca38dda599e3fdd0671671f875ff0e0`  
		Last Modified: Sat, 17 Aug 2024 00:30:23 GMT  
		Size: 5.5 MB (5463812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2134cff8ef668c090feb03d489ac007ac01a8989fbd30ad98d991c1c23562a9`  
		Last Modified: Sat, 17 Aug 2024 00:30:23 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32985400680dfa2c6cf74d1835eea14ae2fc73b54907ca52b7b10113119d92fc`  
		Last Modified: Sat, 17 Aug 2024 00:30:24 GMT  
		Size: 47.7 MB (47709520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee833190ca2a93c62a71fa506ccfe011eb5fc68f6a0b01cc57d72e4cea943c81`  
		Last Modified: Sat, 17 Aug 2024 00:30:24 GMT  
		Size: 21.7 MB (21662517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1aab7e6b6870800469b18270c55044cefb3cfc1e1f3ce66946170e6904eb7d`  
		Last Modified: Sat, 17 Aug 2024 00:30:24 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347808e8ef858635813276420f243cea2e691b4b65caa0f5abf7bd61e353d0d0`  
		Last Modified: Sat, 17 Aug 2024 00:30:24 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e809e4e27cecbf4862c68b1ecddd83ffb4b75e344f5dbe9e3039d7cd94883acf`  
		Last Modified: Sat, 17 Aug 2024 00:30:25 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:873be285f9737151ea3a437fde6b849367139e882d20e97de02248f26ef745ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698e64a085ca77efe546452489fff400b505a107ae7353c5d63e4288f334ce3d`

```dockerfile
```

-	Layers:
	-	`sha256:510622ec6be410f3a19cde7cfd1a2ec4f62e38ca0c34d60608683eecc143438d`  
		Last Modified: Sat, 17 Aug 2024 00:30:23 GMT  
		Size: 913.4 KB (913354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:882f63536e6b5e368095704d289b0e49064f7bb5b237156b9c26fd0c4843d579`  
		Last Modified: Sat, 17 Aug 2024 00:30:23 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json
