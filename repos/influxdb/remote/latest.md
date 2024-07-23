## `influxdb:latest`

```console
$ docker pull influxdb@sha256:f984b58f2a81e10b86b1b98ff82a332f6e832500b320bfb896336819e31e7d27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:e5caa85f18216d92d27adb02fb91cfc6c98aac9ecd7355a80efcb558c63f6b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168482883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f26019eadb9acbba9378124cb10170b621c3d3aaad1af8b1a32061ca755df0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV GOSU_VER=1.16
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=2.7.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jul 2024 20:47:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22338516b2c3a384ef121fc1be4117457521cc28b7e49f84d3844566393dcbf4`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 9.8 MB (9786187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac58becbac91dc22721c4bddf5b16a010cc0ac8b78fa9da9c77ea6cbee97e3bb`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e42e673a8ae1ab1d8fc5db3121984aefb2a875239f966f93bac06ca732cc7f8`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ff614d7de17822649a373bf73d773320b1bdb865318678d0b4ef4977131282`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 1.0 MB (1006375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8208204cff517a7b65a51a644ab584848a3370c7daa173aaa3481505bf12268`  
		Last Modified: Tue, 23 Jul 2024 07:14:43 GMT  
		Size: 99.6 MB (99604818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1929499f66d1a530f2797991e2886b1ca096fec9bbfd53f9adbdbd8624a114f1`  
		Last Modified: Tue, 23 Jul 2024 07:14:43 GMT  
		Size: 23.1 MB (23128322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23b9837bf2e93895fedd50a59f58d21b04b2bb1903c3a4501eb8f6163d432c6`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6466f3f77518b31b3654cea74b2328d01a9180754eb9e646bfc989fcd2ad47f0`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aca036d4f9771de5ef76573cad0e3b0d7b85b1ac31b1aa42337d40de8b2e78f`  
		Last Modified: Tue, 23 Jul 2024 07:14:43 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:43fdd95cc12ecd9c5fbd0ceaf2fbeb17e58b2578eca1fe0b5939c1e1327bae1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373e0fe134451558207814192070ce829957f2f6d71acc5313e26ca71afff868`

```dockerfile
```

-	Layers:
	-	`sha256:f6be574d8c745480b11a730d530d10b703c55a6d75425cec12b60ea60d5e0343`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 2.8 MB (2833446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92aa852aed4af10be99849b53ebf64f9f53e41a1ea4c26751666c5f6a06eccb5`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ab4068e140d69eefb8f5134d8443402564857a760c4ac63c4a2640a59c5df8fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162257359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babfb21c041ece360b0ebe226ced2dc006af72520146e2384978f3017d4e108a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV GOSU_VER=1.16
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=2.7.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jul 2024 20:47:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b786576aaeced8d0e3f4629cddc33ef3344b02b423e70f90628575293158876`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 9.6 MB (9585141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e06d2219f0fc643d914caf4964dc79404236a9b66c8f5c5d4fddd70c27bbb5`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af9beabe444dc89beef8e076bd658fb482b85f2548cb732dd5654f9d827158a`  
		Last Modified: Fri, 12 Jul 2024 00:59:20 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582b012d6a97c3b5b46ae224b4773f900ce31fcefcd2445e201c57cedce4fa3c`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67162d043b41d2a09da357e28b87e5692bcf86fe1da5a9098aded9e4685376c4`  
		Last Modified: Fri, 12 Jul 2024 00:59:24 GMT  
		Size: 95.4 MB (95443266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b80ca3e3b97268665dc499c3639e9c915dabbaefe90225f33c4ee06ef6f6aa`  
		Last Modified: Fri, 12 Jul 2024 00:59:23 GMT  
		Size: 21.7 MB (21662524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef963534d0ea920ef82a986acec28d723c959c1c7ae7f4b3524b4accbc36cf9a`  
		Last Modified: Fri, 12 Jul 2024 00:59:22 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36930f0576c0362da87435f16eee2b6a17ff8d5f48f762f94b47ca4e1c41144`  
		Last Modified: Fri, 12 Jul 2024 00:59:22 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9bdede93fcba6ad11c582c806a9dcf9efe2095d22f4a21faf41d99fc87b37f`  
		Last Modified: Fri, 12 Jul 2024 00:59:23 GMT  
		Size: 6.3 KB (6288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:d342327984c78c72d419eeec2121a4e910e18cebca5403a4ea80cce8b476e5af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2805952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65d349eee61c68c824c6b9dfae1c44b5dfb1c7d7a6b002a598038e4dac827f2`

```dockerfile
```

-	Layers:
	-	`sha256:22efa2d1de5ebc19032c4f173980ae813739f9b300f5c189076dfe023fae3d57`  
		Last Modified: Fri, 12 Jul 2024 00:59:21 GMT  
		Size: 2.8 MB (2772109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f7a2c5672308769994adaa03596da27088e67af9012114a696c3cc8d2aa64aa`  
		Last Modified: Fri, 12 Jul 2024 00:59:20 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json
