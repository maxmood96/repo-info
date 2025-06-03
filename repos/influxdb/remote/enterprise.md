## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:00050dd63372fb3d19c075c26ef01de2e4a9f6ba4f0ec17acb3f1a0848b65a30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:cd7a536e0228f2e44fb6c74f482b14966c4188979c25c61ae87fb6e099083992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103275263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b678dc210c369a39fc2ace27df844e672f5e0e727634745d2ce4f4f2877f682c`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:48 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:44:50 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 09:44:51 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=3.1.0
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb3
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV LOG_FILTER=info
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed484eb018e2fbe80a2e768aed14b04d0878d3e7a1a380c4e310fcd06bd9d21`  
		Last Modified: Thu, 29 May 2025 18:03:57 GMT  
		Size: 6.7 MB (6664779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b39e7ba2c44f4ff8d888101a104be250c940dd1894121d3dfe7e8211509b79b`  
		Last Modified: Thu, 29 May 2025 18:03:54 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6604b2aef1898d354ad638b42d22b928f390c4bb5230a9a9381d7673b23a1a17`  
		Last Modified: Thu, 29 May 2025 18:03:57 GMT  
		Size: 66.9 MB (66888827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab70dfa79385b928e75fb80aea4c12bbb1d65aa8906a7ff9263c54cf55dcac83`  
		Last Modified: Thu, 29 May 2025 18:03:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ac4b7a43a9a5d3a0bff10f078121d45d5e2dfa4771b1a9482ea44689d6bf7a`  
		Last Modified: Thu, 29 May 2025 18:03:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:7cddb8ae848aca46a3c726bfd8d073fa12065c85e1ef1314bc8289ba549358be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e2bb56054b8a0fdd9fba9f70dd889256b6023d5290e5ec1b215d0570183650`

```dockerfile
```

-	Layers:
	-	`sha256:72bfe6ad4088fc234a7705c33e1cc96e9027cf43e5269bbe761907958656aa6b`  
		Last Modified: Thu, 29 May 2025 18:03:55 GMT  
		Size: 2.2 MB (2203288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4430ad4ad8ee477586a8decddb600b7d0cadce0254bc08b0f21277e28776af3b`  
		Last Modified: Thu, 29 May 2025 18:03:55 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0d46086d38d16ef0418a77551f66e98c4f0bc7def594ade4dfd8e306be7137a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96342836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed042af4efe792b6203b9912a6223ac97a8d63fd8ed3aa8637115fa29a7691c1`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 28 May 2025 23:57:45 GMT
ARG RELEASE
# Wed, 28 May 2025 23:57:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 23:57:45 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 23:57:45 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 28 May 2025 23:57:45 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 23:57:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 28 May 2025 23:57:45 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_VERSION=3.1.0
# Wed, 28 May 2025 23:57:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 28 May 2025 23:57:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 28 May 2025 23:57:45 GMT
USER influxdb3
# Wed, 28 May 2025 23:57:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 28 May 2025 23:57:45 GMT
ENV LOG_FILTER=info
# Wed, 28 May 2025 23:57:45 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 28 May 2025 23:57:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 28 May 2025 23:57:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Thu, 29 May 2025 06:11:37 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482dc2248542ad585f759b15b9f85e27167e3c6c47fc1456d4412f92d2b4a423`  
		Last Modified: Tue, 03 Jun 2025 05:01:57 GMT  
		Size: 6.7 MB (6675420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3847e841b0f506b2979520cb832f1496a88ad872d8e318581cdfd88d37e32130`  
		Last Modified: Tue, 03 Jun 2025 05:01:57 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0106ae4bd1103da267a53ff4c048e62ecef7db2fcb452a6c74ce27945668f30`  
		Last Modified: Tue, 03 Jun 2025 05:02:24 GMT  
		Size: 60.8 MB (60811392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4884da03c76b48c397891bc34311b85ab0cca07eeaf61d6b6b81934e4aaee98`  
		Last Modified: Tue, 03 Jun 2025 05:02:22 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b35ef54277f35c139de5974a56f262e8582bf12a894585bba1f4eeaaa8e78`  
		Last Modified: Tue, 03 Jun 2025 05:02:22 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:13e8eaf97e06b3b355143f925096df823e5b447cd38b28c06ec822022d6c5b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1231ac25bf1aa055daca3e539da2e9b1d62df97a0f2d57ebbb707f2a60d162`

```dockerfile
```

-	Layers:
	-	`sha256:7f47cbda60f3efe2c6e1d3784f949e1b989b02a85779b81e8ac82f01e6de6cf3`  
		Last Modified: Tue, 03 Jun 2025 05:02:22 GMT  
		Size: 2.2 MB (2204342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c50a2c70c3ed841e71420dc663de62301a6502ce16099cb4ee109e41d3debb3`  
		Last Modified: Tue, 03 Jun 2025 05:02:21 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json
