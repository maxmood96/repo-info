## `influxdb:core`

```console
$ docker pull influxdb@sha256:9aa9e65e851b7bf5f8573765c86dedcf106f6c1c4540e68526c9fc5908d58b64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:0541f1915c0365e216e5c7c9ad359dfd431d659a48ea38fa1b7efe221f971b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97916361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56191da4e4fcb680e5fd37a29a1cc1fbad49e1cc4a48dfac85c1519027fd874`
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
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45d233bca13463d087d78f8628ee0e48246bb2260ddc2e1753b8edf7a60465e`  
		Last Modified: Fri, 16 May 2025 19:10:07 GMT  
		Size: 6.7 MB (6663446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2335e5ccc6e74199b81cac14d25ef86c600701f0cb179af4909be93c76c0b85`  
		Last Modified: Fri, 16 May 2025 19:10:06 GMT  
		Size: 3.6 KB (3648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2929d11995a5be55a68d56cea52f4a5524a83f19a5064bd79181045de67784`  
		Last Modified: Fri, 16 May 2025 19:10:27 GMT  
		Size: 61.5 MB (61531262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b996a11e64194691cec83263137edbf2d5ac286dd80cfba6e8ac9f61e23ccab`  
		Last Modified: Fri, 16 May 2025 19:10:06 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09920d7411dc2b83cd2ba0f66828d637a672c098969a3a96038f742659eb227b`  
		Last Modified: Fri, 16 May 2025 19:10:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:f4366db6a68771db7c80db70c86d8d352d1700165eaf74db8151308928ef8d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70985cac70f460065e4f4404b8a8792f8871d12d05656a0cce1b4fe5785780f4`

```dockerfile
```

-	Layers:
	-	`sha256:3b47a22f93be6a7ff58cd3e2658f9e3e7024019f24a496b4b7aa3ff56b7799dc`  
		Last Modified: Fri, 16 May 2025 20:20:34 GMT  
		Size: 2.2 MB (2203240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9822b6a3d8b69e8a72ef5bb1ed07e7e811727df146971621810ba146ae8919`  
		Last Modified: Fri, 16 May 2025 20:20:34 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:672c4a4221b3406da630526e426d4e4b172cb72179262e990e6a88f1d5099f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90509144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2005ef240f1a4c466d0784802963fa2b166ace199af5fc927753457eb3efaee0`
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
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d3ffcca3dea02f4c8adcd31729621ed8d7e4b7531c23b8cac9775f570b5085`  
		Last Modified: Thu, 08 May 2025 17:41:14 GMT  
		Size: 6.7 MB (6674461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f74b4aeea550ca1632e75aa80f8fa8a2ccff90a4138e9f7d1c3d8333e53e3e`  
		Last Modified: Thu, 08 May 2025 17:41:13 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07863461f8e1c5ae19e31f7cd33f989a24208a6e83bbd372b715442c76c7b68d`  
		Last Modified: Fri, 16 May 2025 19:09:57 GMT  
		Size: 55.0 MB (54983680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e77c07210f0fc32bc01a1f689f570f68d1684537afb8272a0a54dbf781f4b8`  
		Last Modified: Fri, 16 May 2025 19:09:39 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5425d10b3656e5aa3b699869d3b14e9890737e5953d97f93c95130ae739417`  
		Last Modified: Fri, 16 May 2025 19:09:56 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:3fceef544916459184e06b503c25120d859ee98e6327290ee166e5af44b15f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d106116f0cda0f646738472152eb611a392c3f18d5c2694d15c0d276d62ff03d`

```dockerfile
```

-	Layers:
	-	`sha256:71235520c5b8db6cbc081b11126bd944131d82b49f898244ed2ecd97aadc285b`  
		Last Modified: Fri, 16 May 2025 20:20:37 GMT  
		Size: 2.2 MB (2204322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3aef4f0be0364f461cbf8d084add55647775f705ca011344adcd716ba88893e`  
		Last Modified: Fri, 16 May 2025 20:20:38 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json
