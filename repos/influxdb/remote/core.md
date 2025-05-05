## `influxdb:core`

```console
$ docker pull influxdb@sha256:63d59b3fa6d5edd5e563db2295959cc2f2967e609d7849c730f0566300693887
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:8c594c491e0d86d0a5f6e600dcbbbe6cdfdaa72632f78c3bb3195468a42765ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97869872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a231c26e87f4e0e287e045f06e81c618d6c1216170070b449fd052881daaf3`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 18 Apr 2025 17:08:47 GMT
ARG RELEASE
# Fri, 18 Apr 2025 17:08:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 18 Apr 2025 17:08:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 18 Apr 2025 17:08:47 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 18 Apr 2025 17:08:47 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Fri, 18 Apr 2025 17:08:47 GMT
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
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c25b0878552ae4c757e56e0229f34f91ef653db2c6be4f309b97feca2043aa4`  
		Last Modified: Mon, 05 May 2025 16:35:12 GMT  
		Size: 6.7 MB (6663428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc2f94a1d470bb2bb9948223c3db51c964b44b7e7a4a9eaaf6b7352da09f87`  
		Last Modified: Mon, 05 May 2025 16:35:12 GMT  
		Size: 3.6 KB (3645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d814669dcdfa12fb86fd99e2a5015e2a127b23e17018f2970672f50367f18d`  
		Last Modified: Mon, 05 May 2025 16:35:13 GMT  
		Size: 61.5 MB (61484801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b024005a3120a96f9f49fee4f4d44482074972bb73b2f6e993cdff060ff0f66e`  
		Last Modified: Mon, 05 May 2025 16:35:12 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e6040aba1306fa2524d63193d26122ba38d1010f9db7188db8491a915ef501`  
		Last Modified: Mon, 05 May 2025 16:35:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:f03ba4b382c456f6235a2a53bab877ac54244477509837a39f3df8cdeee45432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2196000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b61c394a7b9965c58d932292ea1b2964f423ec8631f199b76f1bfe4c6fd2b63`

```dockerfile
```

-	Layers:
	-	`sha256:c99697860dde932f70300c1860d93d0407907660e0e6960bd4d2e704e13d6632`  
		Last Modified: Mon, 05 May 2025 16:35:12 GMT  
		Size: 2.2 MB (2178409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:889f496ad5ea3eda5e80070327a85f41cd24744853bbdcccfefcc7eb6a214878`  
		Last Modified: Mon, 05 May 2025 16:35:12 GMT  
		Size: 17.6 KB (17591 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

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

### `influxdb:core` - unknown; unknown

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
