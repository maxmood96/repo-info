## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:7ab6964f5a39c436d61c2d7d90a2beef14f7f8637b194e28c650d229ce15bf18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:0ea8988f3e67b6cf0cc4df65964c0fa5fc0ffa7d1a2abdcd7ab9fda0517cb6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116078279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049099d18298971acbc5c9eb0cd99d3825b1b20f8ca17e9b39f1fdc5fd517b69`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 00:49:58 GMT
ARG RELEASE
# Wed, 30 Jul 2025 00:49:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 00:49:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 00:49:58 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 00:49:58 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["/bin/bash"]
# Wed, 30 Jul 2025 00:49:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_VERSION=3.3.0
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
USER influxdb3
# Wed, 30 Jul 2025 00:49:58 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 30 Jul 2025 00:49:58 GMT
ENV LOG_FILTER=info
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd5a47018a9beb4cc985665fcc77e3781e7a0bf570982abd025c5dcfdbd7827`  
		Last Modified: Tue, 12 Aug 2025 18:04:52 GMT  
		Size: 6.7 MB (6665884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f86c5036ab6540f0f2673fe6b713a221a18e321718efd33adf7351858575b95`  
		Last Modified: Tue, 12 Aug 2025 18:04:48 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081c4f32d2574c93c84589e2bad521659e09a68e9b89c6ed414657bc7aa92aeb`  
		Last Modified: Tue, 12 Aug 2025 18:04:57 GMT  
		Size: 79.7 MB (79685051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79d955709737df6cc11ad2e85ae5a5959a5c3628fa8c35cb8737e616b95c9eb`  
		Last Modified: Tue, 12 Aug 2025 18:04:49 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3135b041bb638d4ff7fbd8b01a89226f4b5a8b6fa5915233a61b384e625a7c`  
		Last Modified: Tue, 12 Aug 2025 18:04:48 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:874c8470d2641e662e63cc3ac9fef9c0cf270976bae62beb3edaa5b742bc6223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1893ea921f4f82ac5cef92c4e202325ded0ee78649ac1c9e37be04763b144fd`

```dockerfile
```

-	Layers:
	-	`sha256:9e6b838f34712f80b5216204b5e24dd56118dd94cb0f5af0db40adee43f7a8ed`  
		Last Modified: Tue, 12 Aug 2025 20:20:37 GMT  
		Size: 2.3 MB (2311325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a30fd29efce19d3ca619d01e1925701bf6b93c9040bc568a9381d4ce45f028`  
		Last Modified: Tue, 12 Aug 2025 20:20:37 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4d797bd4e247e57fd11fb79e6945bad7cef66ca1f20a0042092c7361091b8dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103589222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9138520e57c70b17780af770cf89b641248e387dcfe848df0e05b983bb28dd9c`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 00:49:58 GMT
ARG RELEASE
# Wed, 30 Jul 2025 00:49:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 00:49:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 00:49:58 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 00:49:58 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["/bin/bash"]
# Wed, 30 Jul 2025 00:49:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_VERSION=3.3.0
# Wed, 30 Jul 2025 00:49:58 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
USER influxdb3
# Wed, 30 Jul 2025 00:49:58 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 30 Jul 2025 00:49:58 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 30 Jul 2025 00:49:58 GMT
ENV LOG_FILTER=info
# Wed, 30 Jul 2025 00:49:58 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 30 Jul 2025 00:49:58 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 30 Jul 2025 00:49:58 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef5744dd465f6dceb77a971a27bd9dc5c6a4d652bf7e2ed6733f52d3bf6d9a2`  
		Last Modified: Tue, 12 Aug 2025 19:27:54 GMT  
		Size: 6.7 MB (6676323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbea8a9214e4c4ace18238271fe01d8f22d8f2ee67a720bcb25dc902a50c77c`  
		Last Modified: Tue, 12 Aug 2025 19:27:54 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42369187d40c9bdba63651b5e62daacdea3c446eda901117e0453bc19b135816`  
		Last Modified: Tue, 12 Aug 2025 19:28:00 GMT  
		Size: 68.0 MB (68048392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fc7c6d0c810d156995e5a60c771cd5f2f91788294098cf12af410ecb255af0`  
		Last Modified: Tue, 12 Aug 2025 19:27:53 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8cc5f4d6fc03e2bff13c1f98136a6dddd0736a9e216bca8dd25697cc5a5659`  
		Last Modified: Tue, 12 Aug 2025 19:27:53 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:aae438115a2a059a6a6d63170adabf23a96a3dc0238efe381451b01fd890294d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f8cff4a72194fd6abeed9db4b0975b227f6661c7acc4aefae22f6c08d8ba49`

```dockerfile
```

-	Layers:
	-	`sha256:788cf7d764eb715ab13862d3635d9d403f47a3a28122dbd11e0d3170e2feca58`  
		Last Modified: Tue, 12 Aug 2025 20:20:42 GMT  
		Size: 2.3 MB (2312407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:660191d5fafe299ed4ffde43ee0d316f2ffc73a4447eb86f56ded4847071c394`  
		Last Modified: Tue, 12 Aug 2025 20:20:43 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json
