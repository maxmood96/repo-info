## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:fef9d2a45bf8c416367084fff946c300a3262ea1f29c16008feabc01bddbb666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:add1a67a7c6c5f5bc1a06ffb04edde33a58fe99a44d7c38bbdc96fecdd77400f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99929946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a23f5091ffcb07e0e93730bdcff7c46818425e31ccdf063bc3886a54a9bab7`
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
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
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
	-	`sha256:500e9ce5c3805b6fd553d0c97112fa53a1bbd4d3e72ca7fa0653e702cc4801d0`  
		Last Modified: Mon, 05 May 2025 16:35:15 GMT  
		Size: 6.7 MB (6663418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd83ca831c5c0098a87c5bf44d20a81cf65d40597761cd62c0f2debcf9f66acc`  
		Last Modified: Mon, 05 May 2025 16:35:15 GMT  
		Size: 3.6 KB (3647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d4e64b380104a98008f118a27fff13f587ce1826fd4a0260a961df07223d6c`  
		Last Modified: Mon, 05 May 2025 16:35:17 GMT  
		Size: 63.5 MB (63544883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66073ba3461f8e4694211fb5e25b677e9271ddc7c0ad6acde765f9273b81393f`  
		Last Modified: Mon, 05 May 2025 16:35:15 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26edc8caa4cb76491c00b4a20bf568cb40a28fdcc20c5cb24f4936b2b7cb0801`  
		Last Modified: Mon, 05 May 2025 16:35:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:cbf95c2ed8620a183fff04a236e0e4e239d2b0229edbc5432ae7b72a97609eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2196229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817e444c9bb463dcede792ea42ef601852f98db950ece6eb6befa36cfb49c52d`

```dockerfile
```

-	Layers:
	-	`sha256:84e918280439f9dc5f80d803ab2e2bc4e912f9ec2d92ed956718a021854cdd4f`  
		Last Modified: Mon, 05 May 2025 16:35:15 GMT  
		Size: 2.2 MB (2178457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43108f280017b5eac844bef3b5d7ed1f4b965a7d6495d05a2b6a1b2e14bed56b`  
		Last Modified: Mon, 05 May 2025 16:35:15 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1c471e7d078e67fd5d50fc53917e86b080e7058fb76663250c36aec4c67161a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92485804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d04391a1e6c9c5be441ef636b4b689bc365e4e47fb180647de14a114807c49f`
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
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
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
	-	`sha256:fab43e7d169cefc30631800358c79bcb078cfd9f4b9a869f21f5b57027972971`  
		Last Modified: Fri, 18 Apr 2025 18:18:07 GMT  
		Size: 57.0 MB (56960240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0f6e59401c7936ae3726db92b7a90d83ee605ec86b4d6a99d5d45d22c3f4b3`  
		Last Modified: Fri, 18 Apr 2025 18:18:05 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22730394cebdaea2e3ce390119debdb3de3731cbf6141d0c58f0f2961cb74287`  
		Last Modified: Fri, 18 Apr 2025 18:18:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:f4639a9659288a9f980abaa8c6dc4b694f35c025c0b29466533c1acf1fa9b3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2197454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44d1c38d2d58dcaa583ea464675c9aabcd9e4f38a88e3dbd8d2935a0befac1d`

```dockerfile
```

-	Layers:
	-	`sha256:8a4502b715580feaf67623d512728ceffd363f31672c9472459413587f01e207`  
		Last Modified: Fri, 18 Apr 2025 18:18:05 GMT  
		Size: 2.2 MB (2179535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6efd955ac32c215958d519c266512b55bfe957e5ca7469d743ac389a18c41b6a`  
		Last Modified: Fri, 18 Apr 2025 18:18:04 GMT  
		Size: 17.9 KB (17919 bytes)  
		MIME: application/vnd.in-toto+json
