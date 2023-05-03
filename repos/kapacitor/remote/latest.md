## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:6527d1d6055c5b1146a8322d4e5ab0b8bf29e6af1616929fe51ab60b1af3edab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:e6c895a2ef67bbd1c5f0f650bd6d65d0b04e696f595ce2219930e82358f71540
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134145643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62efa283b5808db59beb9973eba8e81bd19a4c32a0c14e42777406e46f1aed3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:29:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:29:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 29 Mar 2023 22:13:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 28 Apr 2023 23:22:51 GMT
ENV KAPACITOR_VERSION=1.6.6
# Fri, 28 Apr 2023 23:22:57 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 28 Apr 2023 23:22:57 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 28 Apr 2023 23:22:57 GMT
EXPOSE 9092
# Fri, 28 Apr 2023 23:22:58 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 28 Apr 2023 23:22:58 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 28 Apr 2023 23:22:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Apr 2023 23:22:58 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7490ba7e16ba382ca21015280e2ee6dad31879a1f043029e350a8e429770f36`  
		Last Modified: Thu, 16 Mar 2023 05:43:15 GMT  
		Size: 3.8 MB (3788671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eeb23ea57c359eecf9e21c40ddb69f738e9121008fd4956d733ba66d3b7eb38`  
		Last Modified: Thu, 16 Mar 2023 05:43:15 GMT  
		Size: 3.6 MB (3561600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0243d3a83218f7395a11fd1cf305fdda5288f2c8d673e2ec7cd277075235d284`  
		Last Modified: Fri, 28 Apr 2023 23:23:27 GMT  
		Size: 30.7 MB (30692706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b1a2d2847db26e49437ed7d53a20ff1035be41b7a2a3f1752d5d9529de7617`  
		Last Modified: Fri, 28 Apr 2023 23:23:56 GMT  
		Size: 65.7 MB (65672248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6936fad1fe5930e916ca1522cdf53b39f5a094b5accb38f4e200c4b900f672a6`  
		Last Modified: Fri, 28 Apr 2023 23:23:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255e83aeec514100e2c5f29609cf5472c65d4a42c4345f769f0a76030de8cac9`  
		Last Modified: Fri, 28 Apr 2023 23:23:49 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:fd8637c1228eb50cf5f9a226f86d175e705572f38053eba3d4058eee650929bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125995091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92d6c6598cff035de8737c99fe263363e373c50e88d82380cf960e953220d02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 23:56:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 14:10:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 03 May 2023 14:10:18 GMT
ENV KAPACITOR_VERSION=1.6.6
# Wed, 03 May 2023 14:10:24 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 03 May 2023 14:10:25 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 03 May 2023 14:10:25 GMT
EXPOSE 9092
# Wed, 03 May 2023 14:10:25 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 03 May 2023 14:10:25 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 03 May 2023 14:10:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 May 2023 14:10:25 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1026f845342a6b9d1ce7fd9eafb77e2f1f29edebd77279101a8dbcf8c6d9dc1d`  
		Last Modified: Wed, 03 May 2023 00:15:25 GMT  
		Size: 7.1 MB (7065779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d123d3a8b02a77eaa4722bc4519550be04423f94bd1a64d9766c78b317e499`  
		Last Modified: Wed, 03 May 2023 14:10:36 GMT  
		Size: 28.9 MB (28872127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda45cfde5f7e38f5448246f9f11a613c4f44d625ba7d09c12190c77e3d64a2d`  
		Last Modified: Wed, 03 May 2023 14:10:50 GMT  
		Size: 61.7 MB (61669174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2f1193370470f52effdf853b25fe024dcb454fd638faf54c8205ecd57c3450`  
		Last Modified: Wed, 03 May 2023 14:10:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7bf8ddec5971b38e6b568b3e0c344e51318ca96c8955f2a7dadb0f3f689983`  
		Last Modified: Wed, 03 May 2023 14:10:44 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
