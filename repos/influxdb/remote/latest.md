## `influxdb:latest`

```console
$ docker pull influxdb@sha256:1b1ee05256183f89dc8941b5c40268c34933264cd87896f5ed0cdff3793e3fe0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:813cce36a766ed3e3280b68b806591e64bbe9178c9c0a9b2ed7043aefd51695a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168524805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eaca693d9271123d11dd9b73a52b9c3e17d7c205b2622ca93655a48d5571c8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 19:42:18 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV GOSU_VER=1.16
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ceb32a7cd49428f5b5a5ecdd1169ca5237a4d72955d6b7133a61840eb79091d`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 9.6 MB (9596628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749e0ee9681ffcf4992ddb24b0513d74c3c5bd6a137f7319242ae00c7a9fb00d`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 5.8 MB (5820921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350078b5827c590786ffa202ff5e7d457f5ce17578e04d1c1e5a86907d8d2e51`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620187628669b47cda0dd9123d6c9ec83be49f919e909674af1b656bd2a4281f`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 1.0 MB (1006367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8498a0a81b137f0f34a91756d025ce39916bc2e1ac403fb93a57e65e68ab25`  
		Last Modified: Tue, 24 Dec 2024 22:27:29 GMT  
		Size: 100.3 MB (100312964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08b3e9f74aa64c19a1b7785476b8b6151394d3ba0fc7a6a2f18c10e2658cbc7`  
		Last Modified: Tue, 24 Dec 2024 22:27:28 GMT  
		Size: 23.5 MB (23546387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05be0669f9759b48fa48b2e11d1e297cf54382244baee56db7d1149c70d06ca`  
		Last Modified: Tue, 24 Dec 2024 22:27:28 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b93f8466c77b915f1de61395ec259eb44b54354c2d53ee034db9f1215f5c420`  
		Last Modified: Tue, 24 Dec 2024 22:27:28 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d47214fe47b1e82ff5c4c4725fd2842f0155566df5b4abdd087474edf165344`  
		Last Modified: Tue, 24 Dec 2024 22:27:29 GMT  
		Size: 6.3 KB (6288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:af0aa27200123ebaae4036cbfa2c7ac252b56fa97dac7c2b75a045461f7ae17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9a0df5d8a90b8bbf29a9f81606240c49c6150b87fc84e91bf18e76ac7e5f57`

```dockerfile
```

-	Layers:
	-	`sha256:47b57e337cbcd6b24047353607188a10889c6b5f0822d71990b542b9c8a9ace1`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 2.8 MB (2848627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ef6de32486cd7c360225f7fab7cc8f77b10dbdc34b79a0efcbd4df782741fa5`  
		Last Modified: Tue, 24 Dec 2024 22:27:27 GMT  
		Size: 33.7 KB (33720 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f528507919a873d4af59706dcafedbd01e957c1f7486072abd303b1eee4e9ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162212081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac17110b2b3580f3394ad8444cbbdef0c5e53fa3a5ea9a9498dee5a131a2116c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Mon, 02 Dec 2024 19:42:18 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV GOSU_VER=1.16
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e504b4b36364039724107851c14f104c17a19a38e418a0dac37d128a0e69b6`  
		Last Modified: Tue, 03 Dec 2024 06:09:52 GMT  
		Size: 9.4 MB (9394137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcde5c722ef11603102f80429919e679e343779251b49afe1973530a8cb6a060`  
		Last Modified: Tue, 03 Dec 2024 06:09:52 GMT  
		Size: 5.5 MB (5463797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee8439e36466d3542ee88849ad3dbedce3a54162587da4e9053e4a761a49864`  
		Last Modified: Tue, 03 Dec 2024 06:09:52 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46f3328aeb781b983224e05fbfb21eda38f3c0e79dfea6de32418defced789a`  
		Last Modified: Tue, 03 Dec 2024 06:09:52 GMT  
		Size: 936.1 KB (936104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9795ff54e844bfd920858c7a0501b7666560d325c7fff294f32ff1a23ec0bea0`  
		Last Modified: Tue, 03 Dec 2024 06:09:55 GMT  
		Size: 96.2 MB (96151336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20a79ea911985e1d4feca2a085cca41755dd8fd5ac415421290af003ead7a`  
		Last Modified: Tue, 03 Dec 2024 06:09:54 GMT  
		Size: 22.2 MB (22197943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438fa6ac7e3ec58642293527be5211f1db13f3c2e68645ef43179e80014da8d`  
		Last Modified: Tue, 03 Dec 2024 06:09:53 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203f4c745b4f8e7c0533486e095fb1586005c4d789beac4aebf4e2672fcb2f15`  
		Last Modified: Tue, 03 Dec 2024 06:09:54 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94d9be7b64ffbe98b28a731152512a078746b49e8ef69672b0856c87e131c55`  
		Last Modified: Tue, 03 Dec 2024 06:09:54 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:83e7f970198be42adea894c456ae20eb1d0d98d9283c4d614875ecd5ae2b85f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2881584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5681eefba42246f114effe8e2c4c63d9b38e81100253fd6ea11472b6f0db808`

```dockerfile
```

-	Layers:
	-	`sha256:54bbe269f45dd4111bc723e868b5cead5c37b85cf95c268b2318529cb1d1240e`  
		Last Modified: Tue, 03 Dec 2024 06:09:52 GMT  
		Size: 2.8 MB (2847682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8454742407bdff4c30c9f41635890ede8036c0cf09874894797c7410832ac9d7`  
		Last Modified: Tue, 03 Dec 2024 06:09:52 GMT  
		Size: 33.9 KB (33902 bytes)  
		MIME: application/vnd.in-toto+json
