## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:71bf9f4ecabca602da288c3e76a429b4327a41c97a36f76a00c627747c0a13cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:b786228a862d08aeb31798b54f4733970943abe8884073e8071c6f7ca5190849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124636527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8f4e5c8c1c64b9df0e05bc670b9db783bac9a1d7fa1d37dec2c97f189ca2bd`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:16 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 13 Nov 2025 23:28:16 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 13 Nov 2025 23:28:21 GMT
ENV INFLUXDB_VERSION=3.6.0
# Thu, 13 Nov 2025 23:28:21 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 13 Nov 2025 23:28:21 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:21 GMT
USER influxdb3
# Thu, 13 Nov 2025 23:28:21 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 13 Nov 2025 23:28:21 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 13 Nov 2025 23:28:21 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 13 Nov 2025 23:28:21 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 13 Nov 2025 23:28:21 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 13 Nov 2025 23:28:21 GMT
ENV LOG_FILTER=info
# Thu, 13 Nov 2025 23:28:21 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 13 Nov 2025 23:28:21 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:21 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd92952dcfd89d938138f0bfcbd89a1048b2316e44910e0da1f8956fd4776739`  
		Last Modified: Thu, 13 Nov 2025 23:28:46 GMT  
		Size: 6.7 MB (6666171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56897d5b5f7c6e4e5ffe9120b406cde0e6c2f17ed28e536b4247458c5f1b8ca`  
		Last Modified: Thu, 13 Nov 2025 23:28:46 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43465e0b0ef5ea2764c4ebfd65cf4e1dba3dbb9fde4c5bd3be2d7c3d619be56b`  
		Last Modified: Thu, 13 Nov 2025 23:28:52 GMT  
		Size: 88.2 MB (88241538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522a170bc1b8c1ef07fe67ed81ce5f1565dcc5b2bfeb6802402e30399b31e929`  
		Last Modified: Thu, 13 Nov 2025 23:28:46 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34aeed4d7323d216b17804fdcd47589f50b7958a1999a7cdcd4a7d590faaf247`  
		Last Modified: Thu, 13 Nov 2025 23:28:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:9a5b34c7cafd7c40db4e38a6768a48bbbfd3978f879f6ab407dec3fdfccab041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fdeb499ec665ffbcb849cf3eb8a9855ffc29a075b75f95b78162c1c13c500ca`

```dockerfile
```

-	Layers:
	-	`sha256:a5329985a2dd5aed9094ea968303dabfbf707e1f8c56ed24eaef374f61e77f0a`  
		Last Modified: Fri, 14 Nov 2025 03:21:25 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e544ceb3ce2bdd1d03ed6755aaf0b25b5e6c6d8d9d4b5d9e92b77188487cb069`  
		Last Modified: Fri, 14 Nov 2025 03:21:28 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:db6d85b3c70ff4219f36bacc34be15d7fd5e2d6d6c76555c936aa0c7d26e1ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (115040223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8659dd4c2e7395fc93d205488154a14ce4824cb50182d12ec4f64e67cbc99f`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:27:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 13 Nov 2025 23:27:32 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 13 Nov 2025 23:27:37 GMT
ENV INFLUXDB_VERSION=3.6.0
# Thu, 13 Nov 2025 23:27:37 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 13 Nov 2025 23:27:37 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:27:37 GMT
USER influxdb3
# Thu, 13 Nov 2025 23:27:37 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 13 Nov 2025 23:27:37 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 13 Nov 2025 23:27:37 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 13 Nov 2025 23:27:37 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 13 Nov 2025 23:27:37 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 13 Nov 2025 23:27:37 GMT
ENV LOG_FILTER=info
# Thu, 13 Nov 2025 23:27:37 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 13 Nov 2025 23:27:37 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 13 Nov 2025 23:27:37 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4ba7d458e8f91e0ca698b63d6ceb5d9f8e666694f0d495a7484b73717657c2`  
		Last Modified: Thu, 13 Nov 2025 23:28:01 GMT  
		Size: 6.7 MB (6676565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2d18cf293d685c9233f4a0cf0282754a05242629cd6e834ca8ba773381ab29`  
		Last Modified: Thu, 13 Nov 2025 23:28:01 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e2bca99991a6dba325d226dde90ab855afeab9bef342b0bebb27cf764c7f45`  
		Last Modified: Thu, 13 Nov 2025 23:28:16 GMT  
		Size: 79.5 MB (79497572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd89ddcab6d4e6d52acb9d02691e0dd0f1db75cce3ff830695fabe51405df72e`  
		Last Modified: Thu, 13 Nov 2025 23:28:01 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ded256462adf97556e9e36d783317030a7fe24a303e3aae9565671822cb80`  
		Last Modified: Thu, 13 Nov 2025 23:28:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:262bbe5c7f5d8ad30187184a422f4a10a85a6e8797dc31421a0fcf1cefd405cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d47f1f93b2cb9c2ba279c24972aadf136660dc08455cd0574d40d28daf9640f`

```dockerfile
```

-	Layers:
	-	`sha256:1c120ff370fb392e35b353015d292fc9cfb34449b8216d6e36ed7a8ee5cab554`  
		Last Modified: Fri, 14 Nov 2025 03:21:33 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:351947743faade7190bde70ae96b47dbda607732ef51a4428c698c8abdbcfcd2`  
		Last Modified: Fri, 14 Nov 2025 03:21:33 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json
