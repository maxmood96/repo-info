<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.6`](#kapacitor16)
-	[`kapacitor:1.6-alpine`](#kapacitor16-alpine)
-	[`kapacitor:1.6.6`](#kapacitor166)
-	[`kapacitor:1.6.6-alpine`](#kapacitor166-alpine)
-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.6`](#kapacitor176)
-	[`kapacitor:1.7.6-alpine`](#kapacitor176-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.6`

```console
$ docker pull kapacitor@sha256:054999c3cf4a70569a4a7d9429feeeac77262cfcbdde8871cfd2ae5d76d5b933
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
$ docker pull kapacitor@sha256:6f643dfa16ff0560207e542bdaa90aad7c0ce2dbc089e897d4d1ee267805863f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135405377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b841b93a37449d9f80b3a08ba28da20f391755eee26dd22df5e034727766f4`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc402370d6ae517f6c8127317462bd2a2fbadfc4283d28383223f04c7fe7f028`  
		Last Modified: Wed, 09 Apr 2025 06:09:41 GMT  
		Size: 7.0 MB (7048964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84134d11fd4f324b6d348c78c76e0161b0ebedcab69e53e205b1a93583172556`  
		Last Modified: Wed, 09 Apr 2025 15:07:53 GMT  
		Size: 39.3 MB (39331572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a0ca38d080655054093f8f59000abdcd2b39c3a94b0ae59199cda94bce56f7`  
		Last Modified: Wed, 09 Apr 2025 15:07:54 GMT  
		Size: 61.7 MB (61670153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70376743068d36321d36bc65abc29cd2a24287733b4f2d361cc7668350b01856`  
		Last Modified: Wed, 09 Apr 2025 15:07:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679410b01ad3e842ecaaf5d5687724b1762508097b82cdebaa0b306367130ab0`  
		Last Modified: Wed, 09 Apr 2025 15:07:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:661b905709fb722118167d939a31bdc1cec86dca9595becf9cf3fb39b8e083ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05093eccc1b355815238d5a0b274d44ac52b4049bd791233ff0742fa169d6db1`

```dockerfile
```

-	Layers:
	-	`sha256:7ab2561989331aa3e9798ac8ab4f29e9ff7754ece7b84f96011b66f47c173600`  
		Last Modified: Wed, 09 Apr 2025 15:07:52 GMT  
		Size: 3.5 MB (3548748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10e8cffa9d0371335af79f75634afe2eead16a641c0b328b5f4439283100b21e`  
		Last Modified: Wed, 09 Apr 2025 15:07:52 GMT  
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
$ docker pull kapacitor@sha256:054999c3cf4a70569a4a7d9429feeeac77262cfcbdde8871cfd2ae5d76d5b933
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
$ docker pull kapacitor@sha256:6f643dfa16ff0560207e542bdaa90aad7c0ce2dbc089e897d4d1ee267805863f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135405377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b841b93a37449d9f80b3a08ba28da20f391755eee26dd22df5e034727766f4`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc402370d6ae517f6c8127317462bd2a2fbadfc4283d28383223f04c7fe7f028`  
		Last Modified: Wed, 09 Apr 2025 06:09:41 GMT  
		Size: 7.0 MB (7048964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84134d11fd4f324b6d348c78c76e0161b0ebedcab69e53e205b1a93583172556`  
		Last Modified: Wed, 09 Apr 2025 15:07:53 GMT  
		Size: 39.3 MB (39331572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a0ca38d080655054093f8f59000abdcd2b39c3a94b0ae59199cda94bce56f7`  
		Last Modified: Wed, 09 Apr 2025 15:07:54 GMT  
		Size: 61.7 MB (61670153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70376743068d36321d36bc65abc29cd2a24287733b4f2d361cc7668350b01856`  
		Last Modified: Wed, 09 Apr 2025 15:07:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679410b01ad3e842ecaaf5d5687724b1762508097b82cdebaa0b306367130ab0`  
		Last Modified: Wed, 09 Apr 2025 15:07:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:661b905709fb722118167d939a31bdc1cec86dca9595becf9cf3fb39b8e083ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05093eccc1b355815238d5a0b274d44ac52b4049bd791233ff0742fa169d6db1`

```dockerfile
```

-	Layers:
	-	`sha256:7ab2561989331aa3e9798ac8ab4f29e9ff7754ece7b84f96011b66f47c173600`  
		Last Modified: Wed, 09 Apr 2025 15:07:52 GMT  
		Size: 3.5 MB (3548748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10e8cffa9d0371335af79f75634afe2eead16a641c0b328b5f4439283100b21e`  
		Last Modified: Wed, 09 Apr 2025 15:07:52 GMT  
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
$ docker pull kapacitor@sha256:6cf74cae256588a6bb341238b602bf8d883109eed21af2ad641f4a685fac8a3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:c78c945cd2e027d32b1f46d1bd92e2f040c81224c6fff999e649c33fb72e800a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151583590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afc46c91512ccd90b9c285426103c2f523ed08b0dc5511165b902ae185886f3`
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
ENV KAPACITOR_VERSION=1.7.6
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
	-	`sha256:9d99151692ac1e4f56f7304bb8e32c0332b336db15e97128bfddf4cb3739310c`  
		Last Modified: Mon, 05 May 2025 17:03:00 GMT  
		Size: 42.9 MB (42899822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e9734917aa5c35b96b7fcee8d92d6ec0fd3b70f312591a3b7071f29ddfc30`  
		Last Modified: Mon, 05 May 2025 17:03:01 GMT  
		Size: 72.0 MB (72047661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb5a80614fdaa0a3c42c376ecf939bc881bd0cb51d5c6215489eb7f354542d8`  
		Last Modified: Mon, 05 May 2025 17:03:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d867710d58d2db6c53e6d44f3a07d053d64500737ba30a1d5d4081d755d653f`  
		Last Modified: Mon, 05 May 2025 17:02:59 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:16d9b63d679a3aaa85303f1900e40d09ac018f2e3bc030c3b5002db480d4cb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853167cea25a8681110474ab6cf68ac119f98538356f00d471aacd669d9f214f`

```dockerfile
```

-	Layers:
	-	`sha256:eaf90375632e4348420b6b7d6fea8acf6d23e604348fafe276428a092e48390b`  
		Last Modified: Mon, 05 May 2025 17:03:00 GMT  
		Size: 3.6 MB (3556537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbc496b2bb211c2fa3735f0791dfe0f2476008db2b0a59d1e594129ce2b8c97a`  
		Last Modified: Mon, 05 May 2025 17:02:59 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:7968802b11027efd75585fd5c67b401dc6b66b6719b103867e469567349ae7e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141557625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b2faf5388ca995467f72490e01e97c771d5befa1216812e60ca4bcba97a03f`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.7.6
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc402370d6ae517f6c8127317462bd2a2fbadfc4283d28383223f04c7fe7f028`  
		Last Modified: Wed, 09 Apr 2025 06:09:41 GMT  
		Size: 7.0 MB (7048964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84134d11fd4f324b6d348c78c76e0161b0ebedcab69e53e205b1a93583172556`  
		Last Modified: Wed, 09 Apr 2025 15:07:53 GMT  
		Size: 39.3 MB (39331572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7438d6e5d76f4ba6e77463626bd4c17626ef5cbef5c077d14643f9cc4ab68f32`  
		Last Modified: Wed, 09 Apr 2025 15:08:22 GMT  
		Size: 67.8 MB (67822336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405f3c2dc9bdc0052c108f160a8ac18361644e71946657eb2b1f903985185eae`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f62b69160052bf66e94cff1b9fad11a7654eb37b08e7175a5dd8750e696dfcf`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:8c04f410d250a21da66a36ec0616d33926b1dea03519b1d40f568578980f0dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276be6b62852263681cb396ee272a3551513be0871bd17aaba14a267cb12b61b`

```dockerfile
```

-	Layers:
	-	`sha256:859519599cb85ac1966941075c45a9e4494a6efc6061f95fe07ff07b49d9f756`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 3.6 MB (3556011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4cdf2c52d1fff236dc644c19a405aab2ac8e67fee57f5be90b4d29924398b30`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 15.2 KB (15169 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:ab41660e813c337788470adabc9bdc83014a9a838591b5a84e2bea5420dfff0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:d80de5fb0b681e20ec4639fa4f833fe0b2ba22debc1be07411e80f39c8378592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75905011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfd8adc999d9645747e81838530954dcc7416818771d3f40743b7298ae567fc`
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
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.7.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
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
	-	`sha256:bb66ce059e2c58cd1bca56470e6a25e8e94d630ab09f2c0cc3141d879c460143`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff82a75234ac7a2c67a34f6e7192f115d5e12e206035e59917e47237ca12cae`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 296.5 KB (296501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f13695363bccb9f665399c139ff913d5a2ed7e4ee6208ef774f829ea457c6c`  
		Last Modified: Fri, 14 Feb 2025 19:13:08 GMT  
		Size: 72.0 MB (71980833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667ef208e5bab47062223cab49f2e19071361ea8eedad28a206903e51d10b243`  
		Last Modified: Fri, 14 Feb 2025 19:13:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f630e2ff04bbb88b3e31e88074207828bdf03061654955964de05e394c36e557`  
		Last Modified: Fri, 14 Feb 2025 19:13:07 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7739053a142992f3b94e50635d0eb198c83110a26140d4b75852ba1ce0c51c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.0 KB (384016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590c2694bf70026c8fa8dd67c50dfb9bfa11d0c679791667a23ac1ff5db64258`

```dockerfile
```

-	Layers:
	-	`sha256:584b24fbdeb04a9522b2ac6b8dcd6834cd4ed8406d9f9d3c986d800cc727731d`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 368.3 KB (368333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16553670a0a3cb59971f6f10e1686b74c1a3804c0b81eb3d9860df537a4c177`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.6`

```console
$ docker pull kapacitor@sha256:6cf74cae256588a6bb341238b602bf8d883109eed21af2ad641f4a685fac8a3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:c78c945cd2e027d32b1f46d1bd92e2f040c81224c6fff999e649c33fb72e800a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151583590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afc46c91512ccd90b9c285426103c2f523ed08b0dc5511165b902ae185886f3`
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
ENV KAPACITOR_VERSION=1.7.6
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
	-	`sha256:9d99151692ac1e4f56f7304bb8e32c0332b336db15e97128bfddf4cb3739310c`  
		Last Modified: Mon, 05 May 2025 17:03:00 GMT  
		Size: 42.9 MB (42899822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e9734917aa5c35b96b7fcee8d92d6ec0fd3b70f312591a3b7071f29ddfc30`  
		Last Modified: Mon, 05 May 2025 17:03:01 GMT  
		Size: 72.0 MB (72047661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb5a80614fdaa0a3c42c376ecf939bc881bd0cb51d5c6215489eb7f354542d8`  
		Last Modified: Mon, 05 May 2025 17:03:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d867710d58d2db6c53e6d44f3a07d053d64500737ba30a1d5d4081d755d653f`  
		Last Modified: Mon, 05 May 2025 17:02:59 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:16d9b63d679a3aaa85303f1900e40d09ac018f2e3bc030c3b5002db480d4cb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853167cea25a8681110474ab6cf68ac119f98538356f00d471aacd669d9f214f`

```dockerfile
```

-	Layers:
	-	`sha256:eaf90375632e4348420b6b7d6fea8acf6d23e604348fafe276428a092e48390b`  
		Last Modified: Mon, 05 May 2025 17:03:00 GMT  
		Size: 3.6 MB (3556537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbc496b2bb211c2fa3735f0791dfe0f2476008db2b0a59d1e594129ce2b8c97a`  
		Last Modified: Mon, 05 May 2025 17:02:59 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:7968802b11027efd75585fd5c67b401dc6b66b6719b103867e469567349ae7e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141557625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b2faf5388ca995467f72490e01e97c771d5befa1216812e60ca4bcba97a03f`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.7.6
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc402370d6ae517f6c8127317462bd2a2fbadfc4283d28383223f04c7fe7f028`  
		Last Modified: Wed, 09 Apr 2025 06:09:41 GMT  
		Size: 7.0 MB (7048964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84134d11fd4f324b6d348c78c76e0161b0ebedcab69e53e205b1a93583172556`  
		Last Modified: Wed, 09 Apr 2025 15:07:53 GMT  
		Size: 39.3 MB (39331572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7438d6e5d76f4ba6e77463626bd4c17626ef5cbef5c077d14643f9cc4ab68f32`  
		Last Modified: Wed, 09 Apr 2025 15:08:22 GMT  
		Size: 67.8 MB (67822336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405f3c2dc9bdc0052c108f160a8ac18361644e71946657eb2b1f903985185eae`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f62b69160052bf66e94cff1b9fad11a7654eb37b08e7175a5dd8750e696dfcf`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:8c04f410d250a21da66a36ec0616d33926b1dea03519b1d40f568578980f0dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276be6b62852263681cb396ee272a3551513be0871bd17aaba14a267cb12b61b`

```dockerfile
```

-	Layers:
	-	`sha256:859519599cb85ac1966941075c45a9e4494a6efc6061f95fe07ff07b49d9f756`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 3.6 MB (3556011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4cdf2c52d1fff236dc644c19a405aab2ac8e67fee57f5be90b4d29924398b30`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 15.2 KB (15169 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.6-alpine`

```console
$ docker pull kapacitor@sha256:ab41660e813c337788470adabc9bdc83014a9a838591b5a84e2bea5420dfff0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:d80de5fb0b681e20ec4639fa4f833fe0b2ba22debc1be07411e80f39c8378592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75905011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfd8adc999d9645747e81838530954dcc7416818771d3f40743b7298ae567fc`
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
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.7.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
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
	-	`sha256:bb66ce059e2c58cd1bca56470e6a25e8e94d630ab09f2c0cc3141d879c460143`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff82a75234ac7a2c67a34f6e7192f115d5e12e206035e59917e47237ca12cae`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 296.5 KB (296501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f13695363bccb9f665399c139ff913d5a2ed7e4ee6208ef774f829ea457c6c`  
		Last Modified: Fri, 14 Feb 2025 19:13:08 GMT  
		Size: 72.0 MB (71980833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667ef208e5bab47062223cab49f2e19071361ea8eedad28a206903e51d10b243`  
		Last Modified: Fri, 14 Feb 2025 19:13:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f630e2ff04bbb88b3e31e88074207828bdf03061654955964de05e394c36e557`  
		Last Modified: Fri, 14 Feb 2025 19:13:07 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7739053a142992f3b94e50635d0eb198c83110a26140d4b75852ba1ce0c51c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.0 KB (384016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590c2694bf70026c8fa8dd67c50dfb9bfa11d0c679791667a23ac1ff5db64258`

```dockerfile
```

-	Layers:
	-	`sha256:584b24fbdeb04a9522b2ac6b8dcd6834cd4ed8406d9f9d3c986d800cc727731d`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 368.3 KB (368333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16553670a0a3cb59971f6f10e1686b74c1a3804c0b81eb3d9860df537a4c177`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:ab41660e813c337788470adabc9bdc83014a9a838591b5a84e2bea5420dfff0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:d80de5fb0b681e20ec4639fa4f833fe0b2ba22debc1be07411e80f39c8378592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75905011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfd8adc999d9645747e81838530954dcc7416818771d3f40743b7298ae567fc`
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
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.7.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
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
	-	`sha256:bb66ce059e2c58cd1bca56470e6a25e8e94d630ab09f2c0cc3141d879c460143`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff82a75234ac7a2c67a34f6e7192f115d5e12e206035e59917e47237ca12cae`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 296.5 KB (296501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f13695363bccb9f665399c139ff913d5a2ed7e4ee6208ef774f829ea457c6c`  
		Last Modified: Fri, 14 Feb 2025 19:13:08 GMT  
		Size: 72.0 MB (71980833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667ef208e5bab47062223cab49f2e19071361ea8eedad28a206903e51d10b243`  
		Last Modified: Fri, 14 Feb 2025 19:13:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f630e2ff04bbb88b3e31e88074207828bdf03061654955964de05e394c36e557`  
		Last Modified: Fri, 14 Feb 2025 19:13:07 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7739053a142992f3b94e50635d0eb198c83110a26140d4b75852ba1ce0c51c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.0 KB (384016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590c2694bf70026c8fa8dd67c50dfb9bfa11d0c679791667a23ac1ff5db64258`

```dockerfile
```

-	Layers:
	-	`sha256:584b24fbdeb04a9522b2ac6b8dcd6834cd4ed8406d9f9d3c986d800cc727731d`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 368.3 KB (368333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16553670a0a3cb59971f6f10e1686b74c1a3804c0b81eb3d9860df537a4c177`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:6cf74cae256588a6bb341238b602bf8d883109eed21af2ad641f4a685fac8a3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:c78c945cd2e027d32b1f46d1bd92e2f040c81224c6fff999e649c33fb72e800a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151583590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afc46c91512ccd90b9c285426103c2f523ed08b0dc5511165b902ae185886f3`
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
ENV KAPACITOR_VERSION=1.7.6
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
	-	`sha256:9d99151692ac1e4f56f7304bb8e32c0332b336db15e97128bfddf4cb3739310c`  
		Last Modified: Mon, 05 May 2025 17:03:00 GMT  
		Size: 42.9 MB (42899822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e9734917aa5c35b96b7fcee8d92d6ec0fd3b70f312591a3b7071f29ddfc30`  
		Last Modified: Mon, 05 May 2025 17:03:01 GMT  
		Size: 72.0 MB (72047661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb5a80614fdaa0a3c42c376ecf939bc881bd0cb51d5c6215489eb7f354542d8`  
		Last Modified: Mon, 05 May 2025 17:03:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d867710d58d2db6c53e6d44f3a07d053d64500737ba30a1d5d4081d755d653f`  
		Last Modified: Mon, 05 May 2025 17:02:59 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:16d9b63d679a3aaa85303f1900e40d09ac018f2e3bc030c3b5002db480d4cb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853167cea25a8681110474ab6cf68ac119f98538356f00d471aacd669d9f214f`

```dockerfile
```

-	Layers:
	-	`sha256:eaf90375632e4348420b6b7d6fea8acf6d23e604348fafe276428a092e48390b`  
		Last Modified: Mon, 05 May 2025 17:03:00 GMT  
		Size: 3.6 MB (3556537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbc496b2bb211c2fa3735f0791dfe0f2476008db2b0a59d1e594129ce2b8c97a`  
		Last Modified: Mon, 05 May 2025 17:02:59 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:7968802b11027efd75585fd5c67b401dc6b66b6719b103867e469567349ae7e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141557625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b2faf5388ca995467f72490e01e97c771d5befa1216812e60ca4bcba97a03f`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.7.6
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc402370d6ae517f6c8127317462bd2a2fbadfc4283d28383223f04c7fe7f028`  
		Last Modified: Wed, 09 Apr 2025 06:09:41 GMT  
		Size: 7.0 MB (7048964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84134d11fd4f324b6d348c78c76e0161b0ebedcab69e53e205b1a93583172556`  
		Last Modified: Wed, 09 Apr 2025 15:07:53 GMT  
		Size: 39.3 MB (39331572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7438d6e5d76f4ba6e77463626bd4c17626ef5cbef5c077d14643f9cc4ab68f32`  
		Last Modified: Wed, 09 Apr 2025 15:08:22 GMT  
		Size: 67.8 MB (67822336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405f3c2dc9bdc0052c108f160a8ac18361644e71946657eb2b1f903985185eae`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f62b69160052bf66e94cff1b9fad11a7654eb37b08e7175a5dd8750e696dfcf`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:8c04f410d250a21da66a36ec0616d33926b1dea03519b1d40f568578980f0dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276be6b62852263681cb396ee272a3551513be0871bd17aaba14a267cb12b61b`

```dockerfile
```

-	Layers:
	-	`sha256:859519599cb85ac1966941075c45a9e4494a6efc6061f95fe07ff07b49d9f756`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 3.6 MB (3556011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4cdf2c52d1fff236dc644c19a405aab2ac8e67fee57f5be90b4d29924398b30`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 15.2 KB (15169 bytes)  
		MIME: application/vnd.in-toto+json
