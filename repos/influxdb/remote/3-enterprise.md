## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:a1944483af83406ee1b2ebdb66f20a704c311571dedc92aeacd46de46895dae2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6f8ea6dcb55362b0d132b7f69922d834a13d1e7922bcaa8278f412ba0e6f5888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103272989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0b28dfdebea55635b41ec4b137cc3865c987f2b3a8328a0255651a0f5f283c`
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
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
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
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c21a2128df4c0b3a1a2a3a7451bc55de7acd7667af0c240008a2de740bc3c21`  
		Last Modified: Tue, 03 Jun 2025 13:30:50 GMT  
		Size: 6.7 MB (6664721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcf4966be8170f2e514212b42f0941cc3bc0884771a3c37f15ecdd9ae506cfd`  
		Last Modified: Tue, 03 Jun 2025 13:30:49 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cddcd3193a56e570adb2aae85fd9003a155a3a33efd539baf6472a26926b660`  
		Last Modified: Tue, 03 Jun 2025 13:30:54 GMT  
		Size: 66.9 MB (66888800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adf62a59e48bd026bbd4e6e1f76ee899422645120d9f727cf59f86f3c7cba7d`  
		Last Modified: Tue, 03 Jun 2025 13:30:51 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc677efed44bfe802ade6813bf557d4176a30e17bb52c80f5a55a9d22c92269`  
		Last Modified: Tue, 03 Jun 2025 13:30:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:58c92711cc95e02318be2536aeccb756ce6e1136ec91c1e9195f8ae0fbbdccc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2fc48d31a60cdcceafb5c3e408e1a4ad7ba8c8020ed845f9605aa013ac4852b`

```dockerfile
```

-	Layers:
	-	`sha256:023afb9e0f1e8d258db1fea55efffc04398e06410645b1ad839a17868498398e`  
		Last Modified: Sun, 08 Jun 2025 12:29:41 GMT  
		Size: 2.2 MB (2203260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f205c8b6ef888b50c090dc278e429864438a6d7b54fd3a3a6fbe7282bc257604`  
		Last Modified: Sun, 08 Jun 2025 12:29:43 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

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
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482dc2248542ad585f759b15b9f85e27167e3c6c47fc1456d4412f92d2b4a423`  
		Last Modified: Tue, 03 Jun 2025 14:03:42 GMT  
		Size: 6.7 MB (6675420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3847e841b0f506b2979520cb832f1496a88ad872d8e318581cdfd88d37e32130`  
		Last Modified: Tue, 03 Jun 2025 14:03:41 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0106ae4bd1103da267a53ff4c048e62ecef7db2fcb452a6c74ce27945668f30`  
		Last Modified: Wed, 04 Jun 2025 22:07:44 GMT  
		Size: 60.8 MB (60811392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4884da03c76b48c397891bc34311b85ab0cca07eeaf61d6b6b81934e4aaee98`  
		Last Modified: Wed, 04 Jun 2025 22:07:40 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b35ef54277f35c139de5974a56f262e8582bf12a894585bba1f4eeaaa8e78`  
		Last Modified: Wed, 04 Jun 2025 22:07:40 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

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
