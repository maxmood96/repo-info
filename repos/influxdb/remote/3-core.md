## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:dcf3eb8503cc5b40ce5306d527e31441fb81c3b47c4ecbf258e2bcc5c19a00d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:ed9f5a6abaa3621b2151d2d32c81b7331f68fcd4a6ef9ed2a6080f4059fe9a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115499447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b2a76993f080c2e75724a8e27d8565029d6f631d01cb07e4f96d20728d0d19`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75031e697ac0e624e40badbd92e13f49aa336172b0f461faf96d3b05718b524d`  
		Last Modified: Wed, 02 Jul 2025 03:11:28 GMT  
		Size: 6.7 MB (6664700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07dfc9881acc101e1188d20ea5fe2c27ae4438cb5a023d0ea1607e6cbb6c1271`  
		Last Modified: Wed, 02 Jul 2025 03:11:27 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17006a7628c38893b94b7ab024806524b1afd5efacf643232df49a9845c3f34`  
		Last Modified: Wed, 02 Jul 2025 03:11:31 GMT  
		Size: 79.1 MB (79112250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01f7e5c102324e580ebdb0f7cf6e4640d64c23b9f9b6968f9117973601349b7`  
		Last Modified: Wed, 02 Jul 2025 03:11:28 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b764e96ff53bcaae9bd5245a87e06b8d99c7b9ddfc1e84519e29f1461ee7fa03`  
		Last Modified: Wed, 02 Jul 2025 03:11:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:6f989b7afbf4d66d87d640d732d917ace48ae44ed88fac7cae7165a4ac4e89ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5946d2c0d6f64e570b6992d097def58cde4b2d4bba26a0456bfde676794deb54`

```dockerfile
```

-	Layers:
	-	`sha256:bb2873ba6f4d4aec7e596608539a4583b5f4ce60dc629e0074649bb66675a233`  
		Last Modified: Wed, 02 Jul 2025 08:20:30 GMT  
		Size: 2.3 MB (2311303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dc54336e285a01a4230c212af6c3a9e0f8f7e99b9511b677288ee24a3efbe0c`  
		Last Modified: Wed, 02 Jul 2025 08:20:30 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1de261c7cb46d31622f01c6521e052bbd9bee3a419daedb9be6907c5cf261588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102954134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e416330d538cd981a5fc5ba1ac5435b613194a1def7642ba351b3e7207a378a0`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Tue, 24 Jun 2025 22:21:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_VERSION=3.2.0
# Tue, 24 Jun 2025 22:21:26 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
USER influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 24 Jun 2025 22:21:26 GMT
ENV LOG_FILTER=info
# Tue, 24 Jun 2025 22:21:26 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 24 Jun 2025 22:21:26 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 24 Jun 2025 22:21:26 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c0686a251b16fc8cbd211dd5bf5418ccc2bd75968ab247e18683ffb32d360e`  
		Last Modified: Wed, 02 Jul 2025 05:43:01 GMT  
		Size: 6.7 MB (6675401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929431d0f1ad953782d674eae05c259f14e0a696e1e97ac83b03b176f22ee189`  
		Last Modified: Wed, 02 Jul 2025 05:43:00 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e026c4e3a6fa284245f6be18350bd1aa69f9348b7bd49b0fd723dff1a6f5a481`  
		Last Modified: Wed, 02 Jul 2025 05:43:05 GMT  
		Size: 67.4 MB (67418585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c49dc1c8abee6355ae4589360ff982407452829736cfcbd5cf57c9c9f4ceccb`  
		Last Modified: Wed, 02 Jul 2025 05:43:00 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab8ceded79540dd1ecc2e9fcce3cc38a16f29447efa33302d824213a16a2c0f`  
		Last Modified: Wed, 02 Jul 2025 05:43:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:af3db2cb091abecfe35eeb73677a1890fcef55362872548fbc69e294b6f061fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae3421d5b074ecb2c91f2788f67a4987e63773ebf8486d109ef32c6553f6c78`

```dockerfile
```

-	Layers:
	-	`sha256:bd7da870eb36a0738a5ae626d54577cdbf189c985611f132203270951dbfd25b`  
		Last Modified: Wed, 02 Jul 2025 08:20:34 GMT  
		Size: 2.3 MB (2312385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:986533cbb902c7a42edd2a6ba4d7ca5cc5beb9da1c8637c49988b906acf2f333`  
		Last Modified: Wed, 02 Jul 2025 08:20:35 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json
