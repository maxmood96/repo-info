<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.6`](#kapacitor16)
-	[`kapacitor:1.6-alpine`](#kapacitor16-alpine)
-	[`kapacitor:1.6.6`](#kapacitor166)
-	[`kapacitor:1.6.6-alpine`](#kapacitor166-alpine)
-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.7`](#kapacitor177)
-	[`kapacitor:1.7.7-alpine`](#kapacitor177-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.6`

```console
$ docker pull kapacitor@sha256:f80e43b4647a515a0ce5d0c3bec056279cbfa6fbd8bf370c454fa738d3867a42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:69e47273e50b7cc0358511df04ec78ae8873acf98b6ef3e13ad4258609298a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145208904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1429b10be032a4437ffed5af8ea95a43d731f5fbbfaa1b67c7fb607495ca4334`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.6.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a371f1ee9522de0fd813c4772011abcbcdbb8f39e3cf1285f265032957183988`  
		Last Modified: Mon, 05 May 2025 16:34:22 GMT  
		Size: 7.1 MB (7102973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870574205487b59e31f0d34ba3cc71ea7832b4e64cbbf0e9725dab4f396fa658`  
		Last Modified: Mon, 05 May 2025 17:02:57 GMT  
		Size: 42.9 MB (42899826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54a830fb8d712fda1db9b78fbc6b9ce20523c7175d65012140713b07044c2c0`  
		Last Modified: Mon, 05 May 2025 17:02:58 GMT  
		Size: 65.7 MB (65673038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f763776f0f2b5ebf0ab6bedefd1ffb8243f0c8f09266664e8310eaabd925acc`  
		Last Modified: Mon, 05 May 2025 17:02:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd88f67829719c20236517da49a0fa3483dc8397aa5f12d315fd1d11588c073`  
		Last Modified: Mon, 05 May 2025 17:02:56 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:36a8eabf61c3b257c62f7eb89f8ad865ac0b1e51041b162033ea8354533f0e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f33b6f53d2d321a0546332a2ccf4645c2185eb599c41b820f221e6aab1a1546`

```dockerfile
```

-	Layers:
	-	`sha256:74c98be7e28574a67c007ebba763fde6b3b50cebb9f51dccdc9d21b1fe58c48b`  
		Last Modified: Mon, 05 May 2025 17:02:56 GMT  
		Size: 3.5 MB (3548481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ac5a3a712b5f0b50e65059f4bdd59b4c7bf968e38e4010ec2dd52c34576a26`  
		Last Modified: Mon, 05 May 2025 17:02:56 GMT  
		Size: 14.8 KB (14759 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:704e3864f680111e1f4d47b1788ab69a0a621f7cf15367e51145305343a3fa41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136278326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1435446ac04ea11b5a2e049785231e6010c1da8f5600fd537a807f5ac9a0dc0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.6.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8d379476072addecd776a689c342eba7552fd3b54d1d640a45b2d23c18df19`  
		Last Modified: Mon, 05 May 2025 16:36:00 GMT  
		Size: 7.0 MB (7049030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d01dbee62e3acf388a5dfe469d50f91eda377d5a1bcc4675b0b15c6ed6c5eb9`  
		Last Modified: Mon, 05 May 2025 21:46:16 GMT  
		Size: 40.2 MB (40204448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab6e86b749f07a69d71bd2dad5e18d690498e1c8b69b678c40f869b70445234`  
		Last Modified: Mon, 05 May 2025 21:46:18 GMT  
		Size: 61.7 MB (61670181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612eef48f03b97085f8f40439449ca204c40d4cec4f163261e04f1b78a6f7f54`  
		Last Modified: Mon, 05 May 2025 21:46:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131acdae7cac186430f29782e7a22549a9b7986a0d20ef7f80e587785bdeb960`  
		Last Modified: Mon, 05 May 2025 21:46:15 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:77d8e54b5ab2095df76e33096e2f6dba5d3dee3e4a95ab79eee705f898502369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f040ba4e2c4b203427db16f0b7ead03366a4266dd9458f5dd62a9ab510cc2852`

```dockerfile
```

-	Layers:
	-	`sha256:bb6e55b1b0d34ca4f60592c94f85cf1efc530022e97572e1374597e2b02ae43b`  
		Last Modified: Mon, 05 May 2025 21:46:15 GMT  
		Size: 3.5 MB (3548748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:620c8b2f09d08cb70c0e7d3ab6955f301fb70a34667677efaa4a89ec95ec5468`  
		Last Modified: Mon, 05 May 2025 21:46:15 GMT  
		Size: 14.9 KB (14854 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6-alpine`

```console
$ docker pull kapacitor@sha256:eabd8acf11d549814eaca65a093747b22d7f056e8b8695ba6ba89ecb0eb368c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:acf95a57ee1bd5344bb08d22e94189d38735725f0d445a5e20e321975ac5824e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69502141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6c1556e33f80dbbeb72c104bd18352d9bfcef58d892e69e363d02cdf78f02a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 28 Oct 2024 16:40:55 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.6.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b7c4bcd6376f58b15fa52176845abf5128e2c9151d217518b4bc0dbae467c4`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11769bb0f663d8458ef7ce2717f85df6f471c6a3e71503f4f42dc8b3a04edbde`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 294.4 KB (294381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92cf72361b0dade2ad8c0daee300e7282d512572968ad88ad12a30a66ce40a`  
		Last Modified: Fri, 14 Feb 2025 19:26:31 GMT  
		Size: 65.6 MB (65580130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec75cc769591ab3223bacd6530eb8ec0a52abaa396705ca766e48998fa8ab5e3`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce9bbc84973835a4410eb3dbe59f08279662eccd66fa3d75c37d98ee926b949`  
		Last Modified: Fri, 14 Feb 2025 19:26:31 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:96a7504fd082256e9460b4656393509609395679ca29ee244ef0616f5af19565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.4 KB (373441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc92318d6da0674edbeb7f030464518d1c466d4ceb96293a271417108654e6e`

```dockerfile
```

-	Layers:
	-	`sha256:12a7f472e13033d632c5cdb7aab55ab918a7bee2548ea56b8469b34b12a37bf3`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 358.7 KB (358678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae98ee822f327180c826fe1fbbf733f6098cdc27f8b4684d23c7a6d8bb116831`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 14.8 KB (14763 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6.6`

```console
$ docker pull kapacitor@sha256:f80e43b4647a515a0ce5d0c3bec056279cbfa6fbd8bf370c454fa738d3867a42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.6.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:69e47273e50b7cc0358511df04ec78ae8873acf98b6ef3e13ad4258609298a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145208904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1429b10be032a4437ffed5af8ea95a43d731f5fbbfaa1b67c7fb607495ca4334`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.6.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a371f1ee9522de0fd813c4772011abcbcdbb8f39e3cf1285f265032957183988`  
		Last Modified: Mon, 05 May 2025 16:34:22 GMT  
		Size: 7.1 MB (7102973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870574205487b59e31f0d34ba3cc71ea7832b4e64cbbf0e9725dab4f396fa658`  
		Last Modified: Mon, 05 May 2025 17:02:57 GMT  
		Size: 42.9 MB (42899826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54a830fb8d712fda1db9b78fbc6b9ce20523c7175d65012140713b07044c2c0`  
		Last Modified: Mon, 05 May 2025 17:02:58 GMT  
		Size: 65.7 MB (65673038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f763776f0f2b5ebf0ab6bedefd1ffb8243f0c8f09266664e8310eaabd925acc`  
		Last Modified: Mon, 05 May 2025 17:02:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd88f67829719c20236517da49a0fa3483dc8397aa5f12d315fd1d11588c073`  
		Last Modified: Mon, 05 May 2025 17:02:56 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:36a8eabf61c3b257c62f7eb89f8ad865ac0b1e51041b162033ea8354533f0e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f33b6f53d2d321a0546332a2ccf4645c2185eb599c41b820f221e6aab1a1546`

```dockerfile
```

-	Layers:
	-	`sha256:74c98be7e28574a67c007ebba763fde6b3b50cebb9f51dccdc9d21b1fe58c48b`  
		Last Modified: Mon, 05 May 2025 17:02:56 GMT  
		Size: 3.5 MB (3548481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ac5a3a712b5f0b50e65059f4bdd59b4c7bf968e38e4010ec2dd52c34576a26`  
		Last Modified: Mon, 05 May 2025 17:02:56 GMT  
		Size: 14.8 KB (14759 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.6.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:704e3864f680111e1f4d47b1788ab69a0a621f7cf15367e51145305343a3fa41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136278326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1435446ac04ea11b5a2e049785231e6010c1da8f5600fd537a807f5ac9a0dc0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.6.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8d379476072addecd776a689c342eba7552fd3b54d1d640a45b2d23c18df19`  
		Last Modified: Mon, 05 May 2025 16:36:00 GMT  
		Size: 7.0 MB (7049030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d01dbee62e3acf388a5dfe469d50f91eda377d5a1bcc4675b0b15c6ed6c5eb9`  
		Last Modified: Mon, 05 May 2025 21:46:16 GMT  
		Size: 40.2 MB (40204448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab6e86b749f07a69d71bd2dad5e18d690498e1c8b69b678c40f869b70445234`  
		Last Modified: Mon, 05 May 2025 21:46:18 GMT  
		Size: 61.7 MB (61670181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612eef48f03b97085f8f40439449ca204c40d4cec4f163261e04f1b78a6f7f54`  
		Last Modified: Mon, 05 May 2025 21:46:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131acdae7cac186430f29782e7a22549a9b7986a0d20ef7f80e587785bdeb960`  
		Last Modified: Mon, 05 May 2025 21:46:15 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:77d8e54b5ab2095df76e33096e2f6dba5d3dee3e4a95ab79eee705f898502369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f040ba4e2c4b203427db16f0b7ead03366a4266dd9458f5dd62a9ab510cc2852`

```dockerfile
```

-	Layers:
	-	`sha256:bb6e55b1b0d34ca4f60592c94f85cf1efc530022e97572e1374597e2b02ae43b`  
		Last Modified: Mon, 05 May 2025 21:46:15 GMT  
		Size: 3.5 MB (3548748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:620c8b2f09d08cb70c0e7d3ab6955f301fb70a34667677efaa4a89ec95ec5468`  
		Last Modified: Mon, 05 May 2025 21:46:15 GMT  
		Size: 14.9 KB (14854 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6.6-alpine`

```console
$ docker pull kapacitor@sha256:eabd8acf11d549814eaca65a093747b22d7f056e8b8695ba6ba89ecb0eb368c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.6.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:acf95a57ee1bd5344bb08d22e94189d38735725f0d445a5e20e321975ac5824e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69502141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6c1556e33f80dbbeb72c104bd18352d9bfcef58d892e69e363d02cdf78f02a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 28 Oct 2024 16:40:55 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.6.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b7c4bcd6376f58b15fa52176845abf5128e2c9151d217518b4bc0dbae467c4`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11769bb0f663d8458ef7ce2717f85df6f471c6a3e71503f4f42dc8b3a04edbde`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 294.4 KB (294381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92cf72361b0dade2ad8c0daee300e7282d512572968ad88ad12a30a66ce40a`  
		Last Modified: Fri, 14 Feb 2025 19:26:31 GMT  
		Size: 65.6 MB (65580130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec75cc769591ab3223bacd6530eb8ec0a52abaa396705ca766e48998fa8ab5e3`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce9bbc84973835a4410eb3dbe59f08279662eccd66fa3d75c37d98ee926b949`  
		Last Modified: Fri, 14 Feb 2025 19:26:31 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:96a7504fd082256e9460b4656393509609395679ca29ee244ef0616f5af19565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.4 KB (373441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc92318d6da0674edbeb7f030464518d1c466d4ceb96293a271417108654e6e`

```dockerfile
```

-	Layers:
	-	`sha256:12a7f472e13033d632c5cdb7aab55ab918a7bee2548ea56b8469b34b12a37bf3`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 358.7 KB (358678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae98ee822f327180c826fe1fbbf733f6098cdc27f8b4684d23c7a6d8bb116831`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 14.8 KB (14763 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:0b6484788454c27683886a3b1cbb7ff25abd7d3589ce8ecfda7b317815cfbc11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:611d0cf9b5f641bbb13796b522d4780391689f70887849ad28c900ef053409fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152176109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9a0017c1208e9c9a2ba664fdb98f01650d752c44e74ec2a5202942ef02ec46`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a371f1ee9522de0fd813c4772011abcbcdbb8f39e3cf1285f265032957183988`  
		Last Modified: Mon, 05 May 2025 16:34:22 GMT  
		Size: 7.1 MB (7102973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754cbdb4b2c2391a3205d60ca8e4ebd2a9ee1b1b8f16c20a7a7698a8bbcf4cbd`  
		Last Modified: Wed, 28 May 2025 23:10:03 GMT  
		Size: 43.5 MB (43488806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77137f75b04ccb5eae8075f9b5e1ee2dc7270fc23a54da57ab34dd6d77337e9`  
		Last Modified: Wed, 28 May 2025 23:10:03 GMT  
		Size: 72.1 MB (72051194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e0fbafe873ad1b0ff14603a311e84845c5f20c51d593bd5e8df84a5195f874`  
		Last Modified: Wed, 28 May 2025 23:10:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daada038371a3217edfa1321b2506337b4a829acd73dfe17c25decdf6b5b0958`  
		Last Modified: Wed, 28 May 2025 23:10:02 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:8fb860c0936879821e1427f2209faf6ba8ca24ab481d67c319bbb20f8d59421a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3597721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7422e86e90f63963314413b1985eed6ec4310568fb686a130b9e39fefc8d956`

```dockerfile
```

-	Layers:
	-	`sha256:0307ca7c900927e51ac78f39f9ea24c9ac6a07c8b95fc70f733fe4776e15d6b0`  
		Last Modified: Wed, 28 May 2025 23:10:02 GMT  
		Size: 3.6 MB (3582658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7edfaa87ca850ae8d0702eb04dc84a47d55176bccbb40a819bf67915195efbda`  
		Last Modified: Wed, 28 May 2025 23:10:02 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:9a4029ed77eee67bc081478d4b81650f81913c79eced50af1c5dc4ef0e6cfd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142847392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43aae85ed6be3e220f0204e8bdc0ab14bf4f75458bbe4c4f2a84775030706bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8d379476072addecd776a689c342eba7552fd3b54d1d640a45b2d23c18df19`  
		Last Modified: Mon, 05 May 2025 16:36:00 GMT  
		Size: 7.0 MB (7049030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c05201f0c21400c233526b64a20db03271e48fc6ac776017f714f8b02be083a`  
		Last Modified: Wed, 28 May 2025 23:09:12 GMT  
		Size: 40.6 MB (40629854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afc713541b7e66c901cbc80c79dc5cf5d60cc3fbd26ea02e73f0388d99c40d3`  
		Last Modified: Wed, 28 May 2025 23:09:13 GMT  
		Size: 67.8 MB (67813776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df96e6c6adafe24561355eea7ef49c482975e15d0ff559462c53031920fb2178`  
		Last Modified: Wed, 28 May 2025 23:09:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841e0b648f08b2f1ac40a44f20f854e09ef55cff24d2c45a40e2008549bbba19`  
		Last Modified: Wed, 28 May 2025 23:09:10 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:895da0fdd0e91ff331c329de68935ea279eacc1ba24277f13fa12c6a126c905e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3597302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf80a361ffa1fb478a7a40ae6582ef8652f88e03267d9e8ae6ea959c6d4f3b8`

```dockerfile
```

-	Layers:
	-	`sha256:0e804530c1bdc958e017c2fd0e47463b6857da35821213be551afd9359125bdb`  
		Last Modified: Wed, 28 May 2025 23:09:11 GMT  
		Size: 3.6 MB (3582132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1008259893dc1d08205fda1500f0134de332205b142348391a0812fea6012d67`  
		Last Modified: Wed, 28 May 2025 23:09:10 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:89c0134a1fe8f16be0eb018ec821b2f35d5a28b12b2df9d4fefdd8b4c7531127
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:19c160f01a12c421a9618c032af651e4431e99b950c6e8b40d50d68615c03150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75906650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c09b3fd200d86d3901d6c6992ee87be103eba081d05262b144e827b8373c49e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 28 May 2025 13:09:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8050187616735b3a2eca88508aac28bef5adff25592089a08c2584db65c676`  
		Last Modified: Wed, 28 May 2025 23:09:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1818d7c593b71416e16718e6b8ae7023185be1b8e2a8392d819a70fa98c058`  
		Last Modified: Wed, 28 May 2025 23:09:07 GMT  
		Size: 296.5 KB (296509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d64b53402bf4db19ed5b642d9d2ce5742c41eca4320dd5da1cf2e5192a997c5`  
		Last Modified: Wed, 28 May 2025 23:09:09 GMT  
		Size: 72.0 MB (71982465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85316051b6ae6980fa600e7aad098095c72d879f28f69ab821e0336ea4b2fcb2`  
		Last Modified: Wed, 28 May 2025 23:09:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bc54915f27603d346c83ec9056f3063d97df863106ed951f6f27c86a807cef`  
		Last Modified: Wed, 28 May 2025 23:09:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:1c701c0e3f02c51c0b5a416fe2eeb3515e11fbbad452adcf2a6c750cf1dda44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.1 KB (384135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9313b7324de8a37c1323838da614894068e2e5c005651348296d5318ee9d7d`

```dockerfile
```

-	Layers:
	-	`sha256:9765178dab88f44d5afbb350178567db3bacbce39dbac097bdd793ef4cab928f`  
		Last Modified: Wed, 28 May 2025 23:09:07 GMT  
		Size: 368.5 KB (368451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29329adfb7df227bbd4c8aeb6e7b1af9c3cee347c2b209742b71f506b86e41c8`  
		Last Modified: Wed, 28 May 2025 23:09:07 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7`

```console
$ docker pull kapacitor@sha256:0b6484788454c27683886a3b1cbb7ff25abd7d3589ce8ecfda7b317815cfbc11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:611d0cf9b5f641bbb13796b522d4780391689f70887849ad28c900ef053409fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152176109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9a0017c1208e9c9a2ba664fdb98f01650d752c44e74ec2a5202942ef02ec46`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a371f1ee9522de0fd813c4772011abcbcdbb8f39e3cf1285f265032957183988`  
		Last Modified: Mon, 05 May 2025 16:34:22 GMT  
		Size: 7.1 MB (7102973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754cbdb4b2c2391a3205d60ca8e4ebd2a9ee1b1b8f16c20a7a7698a8bbcf4cbd`  
		Last Modified: Wed, 28 May 2025 23:10:03 GMT  
		Size: 43.5 MB (43488806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77137f75b04ccb5eae8075f9b5e1ee2dc7270fc23a54da57ab34dd6d77337e9`  
		Last Modified: Wed, 28 May 2025 23:10:03 GMT  
		Size: 72.1 MB (72051194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e0fbafe873ad1b0ff14603a311e84845c5f20c51d593bd5e8df84a5195f874`  
		Last Modified: Wed, 28 May 2025 23:10:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daada038371a3217edfa1321b2506337b4a829acd73dfe17c25decdf6b5b0958`  
		Last Modified: Wed, 28 May 2025 23:10:02 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:8fb860c0936879821e1427f2209faf6ba8ca24ab481d67c319bbb20f8d59421a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3597721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7422e86e90f63963314413b1985eed6ec4310568fb686a130b9e39fefc8d956`

```dockerfile
```

-	Layers:
	-	`sha256:0307ca7c900927e51ac78f39f9ea24c9ac6a07c8b95fc70f733fe4776e15d6b0`  
		Last Modified: Wed, 28 May 2025 23:10:02 GMT  
		Size: 3.6 MB (3582658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7edfaa87ca850ae8d0702eb04dc84a47d55176bccbb40a819bf67915195efbda`  
		Last Modified: Wed, 28 May 2025 23:10:02 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:9a4029ed77eee67bc081478d4b81650f81913c79eced50af1c5dc4ef0e6cfd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142847392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43aae85ed6be3e220f0204e8bdc0ab14bf4f75458bbe4c4f2a84775030706bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8d379476072addecd776a689c342eba7552fd3b54d1d640a45b2d23c18df19`  
		Last Modified: Mon, 05 May 2025 16:36:00 GMT  
		Size: 7.0 MB (7049030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c05201f0c21400c233526b64a20db03271e48fc6ac776017f714f8b02be083a`  
		Last Modified: Wed, 28 May 2025 23:09:12 GMT  
		Size: 40.6 MB (40629854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afc713541b7e66c901cbc80c79dc5cf5d60cc3fbd26ea02e73f0388d99c40d3`  
		Last Modified: Wed, 28 May 2025 23:09:13 GMT  
		Size: 67.8 MB (67813776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df96e6c6adafe24561355eea7ef49c482975e15d0ff559462c53031920fb2178`  
		Last Modified: Wed, 28 May 2025 23:09:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841e0b648f08b2f1ac40a44f20f854e09ef55cff24d2c45a40e2008549bbba19`  
		Last Modified: Wed, 28 May 2025 23:09:10 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:895da0fdd0e91ff331c329de68935ea279eacc1ba24277f13fa12c6a126c905e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3597302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf80a361ffa1fb478a7a40ae6582ef8652f88e03267d9e8ae6ea959c6d4f3b8`

```dockerfile
```

-	Layers:
	-	`sha256:0e804530c1bdc958e017c2fd0e47463b6857da35821213be551afd9359125bdb`  
		Last Modified: Wed, 28 May 2025 23:09:11 GMT  
		Size: 3.6 MB (3582132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1008259893dc1d08205fda1500f0134de332205b142348391a0812fea6012d67`  
		Last Modified: Wed, 28 May 2025 23:09:10 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7-alpine`

```console
$ docker pull kapacitor@sha256:89c0134a1fe8f16be0eb018ec821b2f35d5a28b12b2df9d4fefdd8b4c7531127
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:19c160f01a12c421a9618c032af651e4431e99b950c6e8b40d50d68615c03150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75906650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c09b3fd200d86d3901d6c6992ee87be103eba081d05262b144e827b8373c49e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 28 May 2025 13:09:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8050187616735b3a2eca88508aac28bef5adff25592089a08c2584db65c676`  
		Last Modified: Wed, 28 May 2025 23:09:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1818d7c593b71416e16718e6b8ae7023185be1b8e2a8392d819a70fa98c058`  
		Last Modified: Wed, 28 May 2025 23:09:07 GMT  
		Size: 296.5 KB (296509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d64b53402bf4db19ed5b642d9d2ce5742c41eca4320dd5da1cf2e5192a997c5`  
		Last Modified: Wed, 28 May 2025 23:09:09 GMT  
		Size: 72.0 MB (71982465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85316051b6ae6980fa600e7aad098095c72d879f28f69ab821e0336ea4b2fcb2`  
		Last Modified: Wed, 28 May 2025 23:09:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bc54915f27603d346c83ec9056f3063d97df863106ed951f6f27c86a807cef`  
		Last Modified: Wed, 28 May 2025 23:09:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:1c701c0e3f02c51c0b5a416fe2eeb3515e11fbbad452adcf2a6c750cf1dda44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.1 KB (384135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9313b7324de8a37c1323838da614894068e2e5c005651348296d5318ee9d7d`

```dockerfile
```

-	Layers:
	-	`sha256:9765178dab88f44d5afbb350178567db3bacbce39dbac097bdd793ef4cab928f`  
		Last Modified: Wed, 28 May 2025 23:09:07 GMT  
		Size: 368.5 KB (368451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29329adfb7df227bbd4c8aeb6e7b1af9c3cee347c2b209742b71f506b86e41c8`  
		Last Modified: Wed, 28 May 2025 23:09:07 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:89c0134a1fe8f16be0eb018ec821b2f35d5a28b12b2df9d4fefdd8b4c7531127
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:19c160f01a12c421a9618c032af651e4431e99b950c6e8b40d50d68615c03150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75906650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c09b3fd200d86d3901d6c6992ee87be103eba081d05262b144e827b8373c49e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 28 May 2025 13:09:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8050187616735b3a2eca88508aac28bef5adff25592089a08c2584db65c676`  
		Last Modified: Wed, 28 May 2025 23:09:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1818d7c593b71416e16718e6b8ae7023185be1b8e2a8392d819a70fa98c058`  
		Last Modified: Wed, 28 May 2025 23:09:07 GMT  
		Size: 296.5 KB (296509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d64b53402bf4db19ed5b642d9d2ce5742c41eca4320dd5da1cf2e5192a997c5`  
		Last Modified: Wed, 28 May 2025 23:09:09 GMT  
		Size: 72.0 MB (71982465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85316051b6ae6980fa600e7aad098095c72d879f28f69ab821e0336ea4b2fcb2`  
		Last Modified: Wed, 28 May 2025 23:09:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bc54915f27603d346c83ec9056f3063d97df863106ed951f6f27c86a807cef`  
		Last Modified: Wed, 28 May 2025 23:09:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:1c701c0e3f02c51c0b5a416fe2eeb3515e11fbbad452adcf2a6c750cf1dda44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.1 KB (384135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9313b7324de8a37c1323838da614894068e2e5c005651348296d5318ee9d7d`

```dockerfile
```

-	Layers:
	-	`sha256:9765178dab88f44d5afbb350178567db3bacbce39dbac097bdd793ef4cab928f`  
		Last Modified: Wed, 28 May 2025 23:09:07 GMT  
		Size: 368.5 KB (368451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29329adfb7df227bbd4c8aeb6e7b1af9c3cee347c2b209742b71f506b86e41c8`  
		Last Modified: Wed, 28 May 2025 23:09:07 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:0b6484788454c27683886a3b1cbb7ff25abd7d3589ce8ecfda7b317815cfbc11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:611d0cf9b5f641bbb13796b522d4780391689f70887849ad28c900ef053409fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152176109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9a0017c1208e9c9a2ba664fdb98f01650d752c44e74ec2a5202942ef02ec46`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a371f1ee9522de0fd813c4772011abcbcdbb8f39e3cf1285f265032957183988`  
		Last Modified: Mon, 05 May 2025 16:34:22 GMT  
		Size: 7.1 MB (7102973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754cbdb4b2c2391a3205d60ca8e4ebd2a9ee1b1b8f16c20a7a7698a8bbcf4cbd`  
		Last Modified: Wed, 28 May 2025 23:10:03 GMT  
		Size: 43.5 MB (43488806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77137f75b04ccb5eae8075f9b5e1ee2dc7270fc23a54da57ab34dd6d77337e9`  
		Last Modified: Wed, 28 May 2025 23:10:03 GMT  
		Size: 72.1 MB (72051194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e0fbafe873ad1b0ff14603a311e84845c5f20c51d593bd5e8df84a5195f874`  
		Last Modified: Wed, 28 May 2025 23:10:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daada038371a3217edfa1321b2506337b4a829acd73dfe17c25decdf6b5b0958`  
		Last Modified: Wed, 28 May 2025 23:10:02 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:8fb860c0936879821e1427f2209faf6ba8ca24ab481d67c319bbb20f8d59421a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3597721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7422e86e90f63963314413b1985eed6ec4310568fb686a130b9e39fefc8d956`

```dockerfile
```

-	Layers:
	-	`sha256:0307ca7c900927e51ac78f39f9ea24c9ac6a07c8b95fc70f733fe4776e15d6b0`  
		Last Modified: Wed, 28 May 2025 23:10:02 GMT  
		Size: 3.6 MB (3582658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7edfaa87ca850ae8d0702eb04dc84a47d55176bccbb40a819bf67915195efbda`  
		Last Modified: Wed, 28 May 2025 23:10:02 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:9a4029ed77eee67bc081478d4b81650f81913c79eced50af1c5dc4ef0e6cfd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142847392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43aae85ed6be3e220f0204e8bdc0ab14bf4f75458bbe4c4f2a84775030706bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8d379476072addecd776a689c342eba7552fd3b54d1d640a45b2d23c18df19`  
		Last Modified: Mon, 05 May 2025 16:36:00 GMT  
		Size: 7.0 MB (7049030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c05201f0c21400c233526b64a20db03271e48fc6ac776017f714f8b02be083a`  
		Last Modified: Wed, 28 May 2025 23:09:12 GMT  
		Size: 40.6 MB (40629854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afc713541b7e66c901cbc80c79dc5cf5d60cc3fbd26ea02e73f0388d99c40d3`  
		Last Modified: Wed, 28 May 2025 23:09:13 GMT  
		Size: 67.8 MB (67813776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df96e6c6adafe24561355eea7ef49c482975e15d0ff559462c53031920fb2178`  
		Last Modified: Wed, 28 May 2025 23:09:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841e0b648f08b2f1ac40a44f20f854e09ef55cff24d2c45a40e2008549bbba19`  
		Last Modified: Wed, 28 May 2025 23:09:10 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:895da0fdd0e91ff331c329de68935ea279eacc1ba24277f13fa12c6a126c905e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3597302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf80a361ffa1fb478a7a40ae6582ef8652f88e03267d9e8ae6ea959c6d4f3b8`

```dockerfile
```

-	Layers:
	-	`sha256:0e804530c1bdc958e017c2fd0e47463b6857da35821213be551afd9359125bdb`  
		Last Modified: Wed, 28 May 2025 23:09:11 GMT  
		Size: 3.6 MB (3582132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1008259893dc1d08205fda1500f0134de332205b142348391a0812fea6012d67`  
		Last Modified: Wed, 28 May 2025 23:09:10 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json
