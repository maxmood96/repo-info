## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:e97eee79d91402947d7f837ff951d2e46bc4822789d29762f7fe09a417d14abd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:13f0b4dcdfd71cfd0fd16e2cb2c9128fdc25e45741c157d9a8766c2542b0b73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115974556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b059bf14de933fe57d323952d5a7012e8e2e8894ce1546633d2130613d7799cf`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 00:34:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_VERSION=3.4.0
# Wed, 27 Aug 2025 00:34:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
USER influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV LOG_FILTER=info
# Wed, 27 Aug 2025 00:34:47 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 27 Aug 2025 00:34:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 27 Aug 2025 00:34:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cdfc8a1d408d8810643874b24d2a77e76638768a9403b94e7084789a41e2df`  
		Last Modified: Wed, 27 Aug 2025 17:20:37 GMT  
		Size: 6.7 MB (6665822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc452c623f024a6dffab2ed0eda980e28c6d6ae3b7b1e0311694778d30d4f781`  
		Last Modified: Wed, 27 Aug 2025 17:02:37 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5eb169ed24a9802925f19ea9f07900c37d85cae68c28faed075a11bead7997`  
		Last Modified: Wed, 27 Aug 2025 17:20:54 GMT  
		Size: 79.6 MB (79581394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478a741c27067a815444a0d3f4a2ccbb14af5100de237b679788fba32ee790f8`  
		Last Modified: Wed, 27 Aug 2025 17:02:40 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0389d5878b7e1b2ff6d8c5a6effbfa01672ece1f5827e4176afe4be98ee04fc3`  
		Last Modified: Wed, 27 Aug 2025 17:02:43 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:1d66b71fcdb18933ce34ed1c4830ca7f30b76df80d7a22fbf47236ed2c54c80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d41c14677a4716cb29765e9a346bd137b68e28d80a69b97109fcca43ad61e4`

```dockerfile
```

-	Layers:
	-	`sha256:e295deba1a642908561f74f1dcf989c36a5cfda50a3167062c6e5f9f4c64d66a`  
		Last Modified: Wed, 27 Aug 2025 17:20:36 GMT  
		Size: 2.3 MB (2311325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dc157fccebd69cc970178ab6004dd24389f3cb6e4dcc4b5f1bc23854f51a4ed`  
		Last Modified: Wed, 27 Aug 2025 17:20:36 GMT  
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
