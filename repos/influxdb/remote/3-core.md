## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:7bdc98e42508d223a6cdba3677d46b7dd29cf8d13833c2205c5f3d5b8a94bfc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:a61fa624c8fcb7881a7798f699870be404245fac0505b5c1512ca7fe54a1ef76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97869886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878c453261a34c305a5532393a723c96178d55f81e69ed873034900f8b90ead4`
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
# Fri, 18 Apr 2025 17:08:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXDB_VERSION=3.0.1
# Fri, 18 Apr 2025 17:08:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
USER influxdb3
# Fri, 18 Apr 2025 17:08:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 18 Apr 2025 17:08:47 GMT
ENV LOG_FILTER=info
# Fri, 18 Apr 2025 17:08:47 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 18 Apr 2025 17:08:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 18 Apr 2025 17:08:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b6a27b5589e2bd436302713ebef38d83b2a25bbe1a06300bbf36ce9c4070e4`  
		Last Modified: Fri, 18 Apr 2025 18:11:39 GMT  
		Size: 6.7 MB (6663314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8bcf5d05bbf3907119519f1c4695f374302026735c75f8301039610b25f61e`  
		Last Modified: Fri, 18 Apr 2025 18:11:38 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c340e2ce2a0b30776475c3d0bb80ed6e139ea4b9f6bbc5672170aaf28e3a91a`  
		Last Modified: Fri, 18 Apr 2025 18:11:40 GMT  
		Size: 61.5 MB (61484797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7e43b986b42bc06e1f27f69779609578e8b2d3d2eaa07c9febf13114521dfe`  
		Last Modified: Fri, 18 Apr 2025 18:11:38 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda5ae61d98ce8dfe8ec946ea76cc4bbc11cda2573149181f945df6423ba73b9`  
		Last Modified: Fri, 18 Apr 2025 18:11:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:fa91e55b81c18c98985bf3043f3d04f219a5ca958dfe0e4941fd1cc51705ff3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2195997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5750dbd7c8c947c818dd37a30bd944f3adc97ffca1c9651e7944ff9a9850f58`

```dockerfile
```

-	Layers:
	-	`sha256:0267b2fe00604b0f4e1467496df85b5146d6c4954c9a9cb005a3c47aa6e8cbac`  
		Last Modified: Fri, 18 Apr 2025 18:11:39 GMT  
		Size: 2.2 MB (2178405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:353b7ff419b69901b3490844821a39d51558fe1f7dfc85c77e7d89a43497146a`  
		Last Modified: Fri, 18 Apr 2025 18:11:38 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:35e71f81e12b551b0349b26a7a34b18be2c8fb597bbf489b2e621a0ddf0d03a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90488268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e2916d24e2661cd85a6b3d07d12cb2f0847f3343f6de8bdeadddb78d09099c`
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
# Fri, 18 Apr 2025 17:08:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXDB_VERSION=3.0.1
# Fri, 18 Apr 2025 17:08:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
USER influxdb3
# Fri, 18 Apr 2025 17:08:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 18 Apr 2025 17:08:47 GMT
ENV LOG_FILTER=info
# Fri, 18 Apr 2025 17:08:47 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 18 Apr 2025 17:08:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 18 Apr 2025 17:08:47 GMT
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
	-	`sha256:113549ff70b31b18640c6420b8fe6a325beeeac3944fa1118d9e12be25df574f`  
		Last Modified: Fri, 18 Apr 2025 18:17:41 GMT  
		Size: 55.0 MB (54962701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a95636f4bf43c30bcfc0931e1c759d0e4e52338f87a65afbd9838c7e3063d0a`  
		Last Modified: Fri, 18 Apr 2025 18:17:39 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd723a54a85fc8bcbc5f8cef2c4db62f20b8bc213befd0fab1623727fff972f`  
		Last Modified: Fri, 18 Apr 2025 18:17:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:8d59917e9cf855c2093eada0e04df0ec283e67b7cc869ce47b125f612f60dad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2197228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4ad8d61c01c2bed82dfc4cb36d240e16a30c7e6ee1b2bece52bc0caa516d33`

```dockerfile
```

-	Layers:
	-	`sha256:c27b2b6e3c006b389aba818de481e1480758722f5555a5498339ab7c6b3cbafc`  
		Last Modified: Fri, 18 Apr 2025 18:17:39 GMT  
		Size: 2.2 MB (2179487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edb65e9ddd3e47effd82eb4728f921829bf8de6fadbde274736ab63c1e060cf2`  
		Last Modified: Fri, 18 Apr 2025 18:17:39 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json
