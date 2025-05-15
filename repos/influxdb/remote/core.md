## `influxdb:core`

```console
$ docker pull influxdb@sha256:23e36c7f2efe2ae8493541b0b5f641eec24851d6d483efcbb4016ec2992a5a82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:b9a3090cb5bb1052a28eff7836fc882dc52158aaddbd31ec1cf126be8adfb995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97925624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fda32cff3e8014cf7962cfefef97611f4d3136e8920182e5bc9b29eeb9e13d`
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
# Mon, 05 May 2025 15:05:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 05 May 2025 15:05:32 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 05 May 2025 15:05:32 GMT
ENV INFLUXDB_VERSION=3.0.2
# Mon, 05 May 2025 15:05:32 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 05 May 2025 15:05:32 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 05 May 2025 15:05:32 GMT
USER influxdb3
# Mon, 05 May 2025 15:05:32 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 05 May 2025 15:05:32 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 05 May 2025 15:05:32 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 05 May 2025 15:05:32 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 05 May 2025 15:05:32 GMT
ENV LOG_FILTER=info
# Mon, 05 May 2025 15:05:32 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 05 May 2025 15:05:32 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 05 May 2025 15:05:32 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ca454dbabc7d414c907affc805d43ce6fe6761a8a15be9aa3a291990bb2d42`  
		Last Modified: Mon, 05 May 2025 17:27:23 GMT  
		Size: 6.7 MB (6663435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873c1755120d368ad503c037d84683c4d3b74987e5e224f97aeee8d7f3e97619`  
		Last Modified: Mon, 05 May 2025 17:27:23 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37b7036ab376a459ae578d8df93a95df8bf8aaeea1e312da8df2e9cb42b05fc`  
		Last Modified: Mon, 05 May 2025 17:27:24 GMT  
		Size: 61.5 MB (61540530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add0004be8205e5ab844885b2adc3b4d1b52ff4a338bb4cedbcdc7e011a24790`  
		Last Modified: Mon, 05 May 2025 17:27:23 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c250e015e433c75817f14830b69ca62b6bf388282d1391347ea7df655059d956`  
		Last Modified: Mon, 05 May 2025 17:27:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:f73de7ce1d0b881211c0a8d18f531021dc6bd4c522aa8bddbabd82aa440b1a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2196001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f7181ae1972ce2288cb4b454a9c54488089a7715e5d75c8138c661c87a2f2a`

```dockerfile
```

-	Layers:
	-	`sha256:a2ae1f30a877ba8456abe34a57db80172df67ca13a66daa37794583c864de990`  
		Last Modified: Mon, 05 May 2025 17:27:23 GMT  
		Size: 2.2 MB (2178409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33cced8d0b4a64a06695d5426ba667d489f816aa49c372e3ab9c331dc74bff17`  
		Last Modified: Mon, 05 May 2025 17:27:23 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:49ce97af923cf17f8fdda09bad731a09b2fc2113dbf0e0744a53a9fc16182f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90506776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e4f83dd59eaa552eb58c3e5409670745c911ed93b4e53d24f031bfcdb30f04`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:58 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:01 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 09:45:01 GMT
CMD ["/bin/bash"]
# Mon, 05 May 2025 15:05:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 05 May 2025 15:05:32 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 05 May 2025 15:05:32 GMT
ENV INFLUXDB_VERSION=3.0.2
# Mon, 05 May 2025 15:05:32 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 05 May 2025 15:05:32 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 05 May 2025 15:05:32 GMT
USER influxdb3
# Mon, 05 May 2025 15:05:32 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 05 May 2025 15:05:32 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 05 May 2025 15:05:32 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 05 May 2025 15:05:32 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 05 May 2025 15:05:32 GMT
ENV LOG_FILTER=info
# Mon, 05 May 2025 15:05:32 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 05 May 2025 15:05:32 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 05 May 2025 15:05:32 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d3ffcca3dea02f4c8adcd31729621ed8d7e4b7531c23b8cac9775f570b5085`  
		Last Modified: Mon, 05 May 2025 21:30:45 GMT  
		Size: 6.7 MB (6674461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f74b4aeea550ca1632e75aa80f8fa8a2ccff90a4138e9f7d1c3d8333e53e3e`  
		Last Modified: Mon, 05 May 2025 21:30:44 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810bc2a1a32c6db241acb0fe3ce183cc23ba020701b8a8956269989cebecd214`  
		Last Modified: Mon, 05 May 2025 21:30:46 GMT  
		Size: 55.0 MB (54981314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f643c7977fd5ebb9364ccc1f28478700160669fbe50c3e28c3c84ee9ee964fd5`  
		Last Modified: Mon, 05 May 2025 21:30:44 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef20db1395fd006a65dc6db9c8213976474bc2762af8b20413c7006be60c78a3`  
		Last Modified: Mon, 05 May 2025 21:30:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:5d309d1aa4ec368613067ed5ab7db185a02a7a40fcdd869b304089b58f49234d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2197231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b74f09088251203b45199f1dcf81087b4d60e9f330fa90a8e8d2d43875282ab`

```dockerfile
```

-	Layers:
	-	`sha256:8de8f1d06a00ca272c95efb6cc0cbdc65045da002ce4cd17463d9ea433951afc`  
		Last Modified: Mon, 05 May 2025 21:30:45 GMT  
		Size: 2.2 MB (2179491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd44ad27e66093aa60832b0fc4f6a44f4a16c8ee65dd706c0a890996b4c7d502`  
		Last Modified: Mon, 05 May 2025 21:30:44 GMT  
		Size: 17.7 KB (17740 bytes)  
		MIME: application/vnd.in-toto+json
