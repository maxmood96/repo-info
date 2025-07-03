## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:eb5fc1d05cf0937c2fe97bb9ab45ca1b5e5a5ce2b1ee3377e88d5dd3a618a96f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:51ca1c4c21da5d2f45cb25ceec61559c3919f9521802899d0f2b69d5a3a3cb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124839300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4274af6508e5531d0b5672323bf4180613ffe67b84b3d805f4ae8d4350c2729`
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
# Thu, 03 Jul 2025 17:46:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=3.2.1
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV LOG_FILTER=info
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cbb8c7e407a8ed1b6742c78ccf99268ca9a9f4f9461e84334e010d0c3fc6b2`  
		Last Modified: Thu, 03 Jul 2025 18:11:46 GMT  
		Size: 6.7 MB (6664693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bb0d4c62c6f30adba13254138a7c0077325f2b344fec2292e156bf82b154aa`  
		Last Modified: Thu, 03 Jul 2025 18:11:46 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099a272d8885a7c27177e0fa1a5d81bc86b7651a6a6dc811fb2cde96465e7e8`  
		Last Modified: Thu, 03 Jul 2025 18:11:54 GMT  
		Size: 88.5 MB (88452114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fb1fe653059d8f57e6e6535e1b1ad39ac8494ed924ae53f87c13fcb7f93434`  
		Last Modified: Thu, 03 Jul 2025 18:11:47 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ececb2420e7b1089629603bd36c757aac77f2facdff3ce28a66e65f26f23dc0a`  
		Last Modified: Thu, 03 Jul 2025 18:11:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:da923ab8fb0d75f1062303f7b9fc90f73dc1a7d68fc4e2b7b7694212ca5dc303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d055ef4fc120adbb7f6a864e6fc03fe084719bec53966773d388607ac42f112`

```dockerfile
```

-	Layers:
	-	`sha256:b4bd134cf58714e89a7ab27d9bddec3abb746c70050479cddb0f8222854f4e28`  
		Last Modified: Thu, 03 Jul 2025 20:20:43 GMT  
		Size: 2.3 MB (2311351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b795e89f5b04e68672c789647d166c8674b392c335c79373207cbedfcc240fc3`  
		Last Modified: Thu, 03 Jul 2025 20:20:44 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0f3bf598b4dd54a2fef4810b0dc6a9a19dc9b346741698a490dcf62afca4a4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112051988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97200ea52b35f63f93e14a8266421e6b311ba9fae7c9fa09eea879e837b03f0`
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
# Thu, 03 Jul 2025 17:46:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=3.2.1
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
USER influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 03 Jul 2025 17:46:22 GMT
ENV LOG_FILTER=info
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
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
	-	`sha256:f9aff82d27e2e354c914e8229bdae43752f746fcd3a5a0291347ee5f061861ce`  
		Last Modified: Thu, 03 Jul 2025 18:23:17 GMT  
		Size: 76.5 MB (76516437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f235450b5238cc838f09d41e21f3fab325c9dd373696c57c26b34527b5a5e6a3`  
		Last Modified: Thu, 03 Jul 2025 18:23:10 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d438e265e8fcf90be481eff26217ea242fdbb36cc041c6c64c926e7e05a920`  
		Last Modified: Thu, 03 Jul 2025 18:23:10 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:c1cfcd19097d8a713d0addf17608c76e29943679bc9a6914edd4cb2e1c36eebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b187a0f2839da5fe6e87beda84f6078eb8be7bc4f710ea632b45e7919528d3ee`

```dockerfile
```

-	Layers:
	-	`sha256:d50396d28e52e16b20e21903203b11fd26f326edd525664c213a322ea376ec83`  
		Last Modified: Thu, 03 Jul 2025 20:20:48 GMT  
		Size: 2.3 MB (2312433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23062a068ca515ec8b7ce409eaea441db2c9781e141e1cd8ea2d62748bbf3a25`  
		Last Modified: Thu, 03 Jul 2025 20:20:48 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json
