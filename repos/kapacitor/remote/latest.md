## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:9500c79038d3b2a5c5dfb130476d4f245740a85d6e009988f4341a0e1a8a135e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:90b01399bada05355f111ffd6430eebed614a6c298bfd00972f746b7978fd62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147097902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8796162b711324d67dcd574fee63392bfb336ee50024bede76069466eead421`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdd47a1c6e1ac7d610f49064cd95fa387d90f32ec99d5bbc6e6076ddb7d1162`  
		Last Modified: Sat, 17 Aug 2024 01:32:05 GMT  
		Size: 7.1 MB (7091635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbc16744ccdcf41a9f2a5134d023396285b28f13e8f6e80688eedf561f12ba2`  
		Last Modified: Sat, 17 Aug 2024 02:01:05 GMT  
		Size: 38.2 MB (38175629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d29bb25556874c5ca9210098390eb99afb4ef98e0a4eaa59e06cffe6c67dbfa`  
		Last Modified: Sat, 17 Aug 2024 02:01:05 GMT  
		Size: 71.4 MB (71389403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58352e708e24d1b7301ae09225356e087a7193f85126aa19c53007bd178ac71e`  
		Last Modified: Sat, 17 Aug 2024 02:01:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57497b3d468c06c85cb3a82c0352d701dc8dbed3c988b832b5195a8ef06ec37`  
		Last Modified: Sat, 17 Aug 2024 02:01:05 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7171ddd72b3667b7423a9cc869bf286aec10910a5bab0560ee7d607989329875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3550063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cdad31dd7b2436475c390fe55eb029c982b8defe866bd4d972125ef006565f`

```dockerfile
```

-	Layers:
	-	`sha256:e3aaee25b4936b2968f81694b29b608a9a5684e738341b138b53934faec6ab30`  
		Last Modified: Sat, 17 Aug 2024 02:01:04 GMT  
		Size: 3.5 MB (3535156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed9dfd155aacc2b7949551c61fe44108e0e45b66b0d225ea2998fae5ee3e7bf0`  
		Last Modified: Sat, 17 Aug 2024 02:01:04 GMT  
		Size: 14.9 KB (14907 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:11241936e84473ecb762f9ad80e1c1a8fdafeab0ee0c4850ec59b34fc57dbda3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137844294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4194c696552f5753ea15c7364f4af46c0f9c010bfc840f5a59da1c5c34052995`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45a8709da787bbcff9e3e7fbb612c1e49a2ced71990421810ee6ef22d5f2bc4`  
		Last Modified: Sat, 17 Aug 2024 01:25:21 GMT  
		Size: 7.0 MB (7033523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ead049629ee586fb3ba64691f4110a6f8d2a3565a89f8e0ae5e6ff415c60052`  
		Last Modified: Sat, 17 Aug 2024 02:51:00 GMT  
		Size: 35.3 MB (35298028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbb9a2f3be44dba249993ad058ba3129fd175033cdf615161a00f74d1e73d89`  
		Last Modified: Sat, 17 Aug 2024 02:51:34 GMT  
		Size: 67.1 MB (67115113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd744062b4c50d169a2f39815fd7bef3843561d8da5550c3ae0c335f47df253`  
		Last Modified: Sat, 17 Aug 2024 02:51:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b2d5cd75a5e1cd13fa3cb42ba47aa16e7a46f43987bede5a6b5cec5222ac09`  
		Last Modified: Sat, 17 Aug 2024 02:51:32 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:b8af6079122d2fe3e217d1af100dd9fdc93a652bcc48b8fd717014e035c43d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26175166746529508cd039398c34f0e2fd9b6ed835b5535ba2f512f4f6f6605c`

```dockerfile
```

-	Layers:
	-	`sha256:bee97c32b6a17eb5e04982fc7c7c728e21538e647ce153fd0575b7ae4c45102b`  
		Last Modified: Sat, 17 Aug 2024 02:51:33 GMT  
		Size: 3.5 MB (3534639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b8b662ded9ff144db01227c1a00f9a8aefd5a0909ae37a223423349e7ce91d9`  
		Last Modified: Sat, 17 Aug 2024 02:51:32 GMT  
		Size: 15.2 KB (15210 bytes)  
		MIME: application/vnd.in-toto+json
