## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:ac2844b58fa708c0ecacf947341637d61614a839cbd0908be8f92b7c4c760de7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:82473d00b2e4785f486f9e08c1537b930ad44e8195fec6d7ccf9e30811b7a730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115825519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4729737e6dbecd101004ed9a56dc1f815c27d8d8cb7a81c0ccaf4342d6dcef3`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Fri, 12 Sep 2025 10:23:24 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
ENV INFLUXDB_VERSION=3.4.2
# Fri, 12 Sep 2025 10:23:24 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
USER influxdb3
# Fri, 12 Sep 2025 10:23:24 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 12 Sep 2025 10:23:24 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 12 Sep 2025 10:23:24 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 12 Sep 2025 10:23:24 GMT
ENV LOG_FILTER=info
# Fri, 12 Sep 2025 10:23:24 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 12 Sep 2025 10:23:24 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 12 Sep 2025 10:23:24 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39ea4b9b8badbf84ae2089ae04e9582213e681916e5466988ae39d0d0f73fc5`  
		Last Modified: Fri, 12 Sep 2025 17:36:37 GMT  
		Size: 6.7 MB (6665754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ae7d2920f12e1f386f7158c333c7c317ad0c3ba6de5f666025035473f1bc9d`  
		Last Modified: Fri, 12 Sep 2025 17:36:37 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c78de28d930deca62b709c1728f3408a6a3b4fa5788799de092256c6b41b4f`  
		Last Modified: Fri, 12 Sep 2025 17:36:45 GMT  
		Size: 79.4 MB (79432575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0a3834bf9053d5d431c25a396a764f5a22640df4bbb373a436e44d2e73bfe7`  
		Last Modified: Fri, 12 Sep 2025 17:36:36 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5805ec62fdb937e8a4875b52b8c54315031cface20ed3519f55306bba3d394d6`  
		Last Modified: Fri, 12 Sep 2025 17:36:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:af83eca095b054bb7f0161cfac6336ee0fced298c3306310e057253823171013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4306f7ce7ed83f67b8ec0b552ca83c6b56935178458965993900f395ef267d09`

```dockerfile
```

-	Layers:
	-	`sha256:a62994a7b1cc7ee7769fd1ab0234ca054ff04bb8ad98c4b0f6a9b99df994d690`  
		Last Modified: Fri, 12 Sep 2025 20:20:32 GMT  
		Size: 2.3 MB (2311325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91995c92fb88cdb2dd39c4565bbcd1649b2c1e63d34ca0462b0c3c7df993d3cb`  
		Last Modified: Fri, 12 Sep 2025 20:20:33 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f8cfd3ddfc695be3e45c31969486a79821884ee73d65f4fd92ec2119a7ff4250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106589065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c296ecbfe5232e02eadd65f3862df1c4a6ae66b823774b996dc8bc4cd25382`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
CMD ["/bin/bash"]
# Fri, 12 Sep 2025 10:23:24 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
ENV INFLUXDB_VERSION=3.4.2
# Fri, 12 Sep 2025 10:23:24 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
USER influxdb3
# Fri, 12 Sep 2025 10:23:24 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 12 Sep 2025 10:23:24 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 12 Sep 2025 10:23:24 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 12 Sep 2025 10:23:24 GMT
ENV LOG_FILTER=info
# Fri, 12 Sep 2025 10:23:24 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 12 Sep 2025 10:23:24 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 12 Sep 2025 10:23:24 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce7b18b386d30b43df14b4df82f9b459f88018d19e15c57dce41034eae94966`  
		Last Modified: Fri, 12 Sep 2025 17:37:00 GMT  
		Size: 6.7 MB (6676283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac1371131315f2fd1e93a23aac846135a69c2a24f522f416a81400830b21eed`  
		Last Modified: Fri, 12 Sep 2025 17:37:00 GMT  
		Size: 3.7 KB (3658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878a7daa9e838e17f9ba2c9373d01d0c67fa19ab06ca256a0dcd5aded53a6f28`  
		Last Modified: Fri, 12 Sep 2025 17:37:08 GMT  
		Size: 71.0 MB (71048407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02625d68cb51f977f4ed63ee4217415b899877348e3792bb2a02330df078393`  
		Last Modified: Fri, 12 Sep 2025 17:37:00 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0353963aadf15c7e32508169fe079d89d1d7665a1c39dc455a6ea7ed2928149`  
		Last Modified: Fri, 12 Sep 2025 17:37:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:1818f072aa5d59f948208be9df7e50ae15171e43f46c4cb1700ee013237d8255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc410ef6486d751544ac978a88fde495eac68d8909c02487bc97a948899682ef`

```dockerfile
```

-	Layers:
	-	`sha256:f6450d287a3b98107c318acb55f253f7486bffa66b92968c5d1fc2de501193d5`  
		Last Modified: Fri, 12 Sep 2025 20:20:37 GMT  
		Size: 2.3 MB (2312407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1daf263ee8d945a22ff582ed5ba327fd4672a39b66f232c71b1af6ba5bbb246`  
		Last Modified: Fri, 12 Sep 2025 20:20:38 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json
