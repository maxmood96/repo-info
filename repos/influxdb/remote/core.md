## `influxdb:core`

```console
$ docker pull influxdb@sha256:e15eb2d29410471be3688956dbd7307547a8ac8391f7b38f88d8a4968ee06f09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:9bb7760aaa5cdc37918c1bbf4e9d6a2b6cbef1a3ca079c857b7d338670c2d7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97864974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae330df3932fd26366f3e6393425c7e53ecd2d7f0fe2a00d99e9c3d9ef19f0c1`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 20:12:11 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 16 Apr 2025 20:12:11 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 16 Apr 2025 20:12:11 GMT
ENV INFLUXDB_VERSION=3.0.0
# Wed, 16 Apr 2025 20:12:11 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 16 Apr 2025 20:12:11 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 16 Apr 2025 20:12:11 GMT
USER influxdb3
# Wed, 16 Apr 2025 20:12:11 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 16 Apr 2025 20:12:11 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 16 Apr 2025 20:12:11 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 16 Apr 2025 20:12:11 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 16 Apr 2025 20:12:11 GMT
ENV LOG_FILTER=info
# Wed, 16 Apr 2025 20:12:11 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 16 Apr 2025 20:12:11 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 16 Apr 2025 20:12:11 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ad2b9644d2ff33b4d4b189c597cfa8d8828ced141b116e21d3ce60a7d536d6`  
		Last Modified: Thu, 17 Apr 2025 00:22:45 GMT  
		Size: 6.7 MB (6663382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9638757b0b1716581e828572f60d8088bd4186d32c5dfe14c9d548ab0d75f7a1`  
		Last Modified: Thu, 17 Apr 2025 00:22:45 GMT  
		Size: 3.6 KB (3648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb154de16cc1204195b7b27e3abbc60739bdbd880a38356fc42a86fc522e42b`  
		Last Modified: Thu, 17 Apr 2025 00:22:46 GMT  
		Size: 61.5 MB (61479847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5558f96d58da18e3a8164ccd861f1d583b60befbeb289e09e135239c42fe46`  
		Last Modified: Thu, 17 Apr 2025 00:22:45 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effd9a2ffd150636a47e09897f4f305d2a1cfe1f5761c19e53787625a3bf7247`  
		Last Modified: Thu, 17 Apr 2025 00:22:46 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:b292c1d57b4214c64268257b358a0c2af740d5d079647750862e56ef1ab7f592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2195997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7423f8c38dc9c9420bc240530d99216a22f57d23cbbd835d41f176673662527`

```dockerfile
```

-	Layers:
	-	`sha256:0e13bde152756429378ddaa05be2ba31ebf764964a1fcdce2c251f76e8b7efcb`  
		Last Modified: Thu, 17 Apr 2025 00:22:45 GMT  
		Size: 2.2 MB (2178405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b5b268640669951d62940121a91ae3b43ab67e286f799c3cb92ddbbae2c9a3`  
		Last Modified: Thu, 17 Apr 2025 00:22:45 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:278755966a221dee4c2942e943890feac0eeb19e46a22c39c50de1b0d20e8a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90487466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c3cae015a7f77a3df158654aa5cd9aff2dac6a955d4506e7dcad42d0fae244`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 20:12:11 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 16 Apr 2025 20:12:11 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 16 Apr 2025 20:12:11 GMT
ENV INFLUXDB_VERSION=3.0.0
# Wed, 16 Apr 2025 20:12:11 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 16 Apr 2025 20:12:11 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 16 Apr 2025 20:12:11 GMT
USER influxdb3
# Wed, 16 Apr 2025 20:12:11 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 16 Apr 2025 20:12:11 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 16 Apr 2025 20:12:11 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 16 Apr 2025 20:12:11 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 16 Apr 2025 20:12:11 GMT
ENV LOG_FILTER=info
# Wed, 16 Apr 2025 20:12:11 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 16 Apr 2025 20:12:11 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 16 Apr 2025 20:12:11 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8891477565dc5bf23873a4858b1c0e32fc4cbb6ccd5d38b8fbd101d57535bb9`  
		Last Modified: Thu, 17 Apr 2025 00:22:36 GMT  
		Size: 6.7 MB (6674484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa06c2c573052b59002e665de80fabc0fdf212c92aca155bb0caf266e2a3135`  
		Last Modified: Thu, 17 Apr 2025 00:22:36 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001dd1a84b0ccb820f07c352dc9c7e81a916c036c88951dd06b6409cdb8c9c33`  
		Last Modified: Thu, 17 Apr 2025 00:22:38 GMT  
		Size: 55.0 MB (54961923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a59db31e397e4910dd47ea9bf71c87dd6d4b445e1567c9590fd20790ec540b2`  
		Last Modified: Thu, 17 Apr 2025 00:22:36 GMT  
		Size: 299.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445d0b7a85248776b1afc17e3372a3e6723cb838ca6bd8a8e066a65df1c904d2`  
		Last Modified: Thu, 17 Apr 2025 00:22:37 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:b0c0b6afae0a9e59d4b18510cde8ba27bb89772c9d760a3ab893ade6eedb6eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2197227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1badc37eb3b27da1435223712e448fea6b73a44fab9651d109f1721f61df367f`

```dockerfile
```

-	Layers:
	-	`sha256:2c01347bb21a300e8cc100526b3673e5e1c2e07041942183285045085009e838`  
		Last Modified: Thu, 17 Apr 2025 00:22:36 GMT  
		Size: 2.2 MB (2179487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55e7bb89d436adec09f19d4a35bf7270a1b60e5916495989da89fc5e4819d994`  
		Last Modified: Thu, 17 Apr 2025 00:22:36 GMT  
		Size: 17.7 KB (17740 bytes)  
		MIME: application/vnd.in-toto+json
