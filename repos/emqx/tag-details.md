<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:4`](#emqx4)
-	[`emqx:4.3`](#emqx43)
-	[`emqx:4.3.5`](#emqx435)
-	[`emqx:4.4`](#emqx44)
-	[`emqx:4.4.2`](#emqx442)
-	[`emqx:latest`](#emqxlatest)

## `emqx:4`

```console
$ docker pull emqx@sha256:e20e773149bd3e95781cf87409b93cbeb9be5cd4550db79d35e3b075ac8c1b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:d86d9ec27e7d8c28a6e582eddb7e495a5110f345786c98633440a2a8f8f6e40b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124618169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ef1420603b2b042c1a4a2afd1227557c6ea3e7045cd0a8e0b1c301b4335981`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 07:16:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 07:16:43 GMT
ENV EMQX_VERSION=4.4.2
# Wed, 20 Apr 2022 07:16:44 GMT
ENV OTP=otp24.1.5-3
# Wed, 20 Apr 2022 07:16:49 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="bbeb72effcbebab56a3331bdd51dbf5810121d9b2bc57a294d49e97bd9eed7f4"; fi;     if [ ${arch} = "arm64" ]; then sha256="13f6bc6b218f837bb8e7353e5470190152a8c8e19780762ad7fd0c828ef6fb29"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 20 Apr 2022 07:16:54 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 20 Apr 2022 07:16:54 GMT
WORKDIR /opt/emqx
# Wed, 20 Apr 2022 07:16:54 GMT
USER emqx
# Wed, 20 Apr 2022 07:16:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 20 Apr 2022 07:16:54 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 20 Apr 2022 07:16:55 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 20 Apr 2022 07:16:55 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 20 Apr 2022 07:16:55 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a7fa618b3ee98f630ea5fd88bb7bb8b5d6b598c968835215a4c82e3c4cfd4a`  
		Last Modified: Wed, 20 Apr 2022 07:17:22 GMT  
		Size: 2.6 MB (2568085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbceec71e45d6c2b8076974751b5d7f7cfbc56a3de4ca8a914b16bc934c6c62`  
		Last Modified: Wed, 20 Apr 2022 07:17:26 GMT  
		Size: 45.3 MB (45333518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52371626cb7e99f7c6aaebe4553506b25ee848e8bfea4449609181137cd8908d`  
		Last Modified: Wed, 20 Apr 2022 07:17:26 GMT  
		Size: 45.3 MB (45336481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71835fed0df86c8bfa5377adb33e8a60cc98830ed7d3b2a60a377b60ce27b007`  
		Last Modified: Wed, 20 Apr 2022 07:17:21 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3`

```console
$ docker pull emqx@sha256:c7069c557f85388d0369355a150d24a329015e5c30d3bb869eda2d5247377cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `emqx:4.3` - linux; amd64

```console
$ docker pull emqx@sha256:898298246f7a8b4479048b9fe3d56ccd109d914078f1045e119ae57b2e9630b8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62028237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50bbe6c72c3e9e585f7defe9c9a3e5f85bde20b2e52453c1e7bbb737e2b26d6`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 07:16:11 GMT
RUN groupadd -r -g 1000 emqx && useradd -r -m -u 1000 -g emqx emqx
# Wed, 20 Apr 2022 07:16:18 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates curl gnupg;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 07:16:20 GMT
RUN set -eu;     key='FC841BA637755CA8487B1E3CC0B409463E640D53';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";     mkdir -p /etc/apt/keyrings;     gpg --batch --export "$key" > /etc/apt/keyrings/emqx.gpg;     gpgconf --kill all;     rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 07:16:20 GMT
ENV EMQX_VERSION=4.3.5
# Wed, 20 Apr 2022 07:16:33 GMT
RUN set -eu;     echo "deb [signed-by=/etc/apt/keyrings/emqx.gpg] https://repos.emqx.io/emqx-ce/deb/debian/ ./buster stable" >> /etc/apt/sources.list.d/emqx.list;     apt-get update;     apt-get install -y --no-install-recommends emqx="$EMQX_VERSION";     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 07:16:33 GMT
USER emqx
# Wed, 20 Apr 2022 07:16:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 20 Apr 2022 07:16:34 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Wed, 20 Apr 2022 07:16:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 20 Apr 2022 07:16:34 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd2441adca68cbecc6b695526338997163c2d18d5e599bd8624dad27d56e5f0`  
		Last Modified: Wed, 20 Apr 2022 07:17:08 GMT  
		Size: 4.1 KB (4099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84837e560741795741c7de562bb3d47f3c551fa755745dadda9c2c278120c06`  
		Last Modified: Wed, 20 Apr 2022 07:17:10 GMT  
		Size: 8.1 MB (8141522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084771893e235e6c8a14148b2cabf8a455367a17e4d077471b984c1ceb02282d`  
		Last Modified: Wed, 20 Apr 2022 07:17:08 GMT  
		Size: 874.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b45290c6f1412c49c3f3c9cccb8e47d370d0f521977d13ab814b91ee3d3b1f2`  
		Last Modified: Wed, 20 Apr 2022 07:17:11 GMT  
		Size: 26.7 MB (26740037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8b266f0857a37252b5642209c7e00d6d1b9ac72ac068859cc54e33c0d58098`  
		Last Modified: Wed, 20 Apr 2022 07:17:08 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3.5`

```console
$ docker pull emqx@sha256:c7069c557f85388d0369355a150d24a329015e5c30d3bb869eda2d5247377cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `emqx:4.3.5` - linux; amd64

```console
$ docker pull emqx@sha256:898298246f7a8b4479048b9fe3d56ccd109d914078f1045e119ae57b2e9630b8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62028237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50bbe6c72c3e9e585f7defe9c9a3e5f85bde20b2e52453c1e7bbb737e2b26d6`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 07:16:11 GMT
RUN groupadd -r -g 1000 emqx && useradd -r -m -u 1000 -g emqx emqx
# Wed, 20 Apr 2022 07:16:18 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates curl gnupg;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 07:16:20 GMT
RUN set -eu;     key='FC841BA637755CA8487B1E3CC0B409463E640D53';     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";     mkdir -p /etc/apt/keyrings;     gpg --batch --export "$key" > /etc/apt/keyrings/emqx.gpg;     gpgconf --kill all;     rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 07:16:20 GMT
ENV EMQX_VERSION=4.3.5
# Wed, 20 Apr 2022 07:16:33 GMT
RUN set -eu;     echo "deb [signed-by=/etc/apt/keyrings/emqx.gpg] https://repos.emqx.io/emqx-ce/deb/debian/ ./buster stable" >> /etc/apt/sources.list.d/emqx.list;     apt-get update;     apt-get install -y --no-install-recommends emqx="$EMQX_VERSION";     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 07:16:33 GMT
USER emqx
# Wed, 20 Apr 2022 07:16:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 20 Apr 2022 07:16:34 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Wed, 20 Apr 2022 07:16:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 20 Apr 2022 07:16:34 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd2441adca68cbecc6b695526338997163c2d18d5e599bd8624dad27d56e5f0`  
		Last Modified: Wed, 20 Apr 2022 07:17:08 GMT  
		Size: 4.1 KB (4099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84837e560741795741c7de562bb3d47f3c551fa755745dadda9c2c278120c06`  
		Last Modified: Wed, 20 Apr 2022 07:17:10 GMT  
		Size: 8.1 MB (8141522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084771893e235e6c8a14148b2cabf8a455367a17e4d077471b984c1ceb02282d`  
		Last Modified: Wed, 20 Apr 2022 07:17:08 GMT  
		Size: 874.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b45290c6f1412c49c3f3c9cccb8e47d370d0f521977d13ab814b91ee3d3b1f2`  
		Last Modified: Wed, 20 Apr 2022 07:17:11 GMT  
		Size: 26.7 MB (26740037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8b266f0857a37252b5642209c7e00d6d1b9ac72ac068859cc54e33c0d58098`  
		Last Modified: Wed, 20 Apr 2022 07:17:08 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:e20e773149bd3e95781cf87409b93cbeb9be5cd4550db79d35e3b075ac8c1b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:d86d9ec27e7d8c28a6e582eddb7e495a5110f345786c98633440a2a8f8f6e40b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124618169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ef1420603b2b042c1a4a2afd1227557c6ea3e7045cd0a8e0b1c301b4335981`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 07:16:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 07:16:43 GMT
ENV EMQX_VERSION=4.4.2
# Wed, 20 Apr 2022 07:16:44 GMT
ENV OTP=otp24.1.5-3
# Wed, 20 Apr 2022 07:16:49 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="bbeb72effcbebab56a3331bdd51dbf5810121d9b2bc57a294d49e97bd9eed7f4"; fi;     if [ ${arch} = "arm64" ]; then sha256="13f6bc6b218f837bb8e7353e5470190152a8c8e19780762ad7fd0c828ef6fb29"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 20 Apr 2022 07:16:54 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 20 Apr 2022 07:16:54 GMT
WORKDIR /opt/emqx
# Wed, 20 Apr 2022 07:16:54 GMT
USER emqx
# Wed, 20 Apr 2022 07:16:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 20 Apr 2022 07:16:54 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 20 Apr 2022 07:16:55 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 20 Apr 2022 07:16:55 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 20 Apr 2022 07:16:55 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a7fa618b3ee98f630ea5fd88bb7bb8b5d6b598c968835215a4c82e3c4cfd4a`  
		Last Modified: Wed, 20 Apr 2022 07:17:22 GMT  
		Size: 2.6 MB (2568085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbceec71e45d6c2b8076974751b5d7f7cfbc56a3de4ca8a914b16bc934c6c62`  
		Last Modified: Wed, 20 Apr 2022 07:17:26 GMT  
		Size: 45.3 MB (45333518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52371626cb7e99f7c6aaebe4553506b25ee848e8bfea4449609181137cd8908d`  
		Last Modified: Wed, 20 Apr 2022 07:17:26 GMT  
		Size: 45.3 MB (45336481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71835fed0df86c8bfa5377adb33e8a60cc98830ed7d3b2a60a377b60ce27b007`  
		Last Modified: Wed, 20 Apr 2022 07:17:21 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.2`

```console
$ docker pull emqx@sha256:e20e773149bd3e95781cf87409b93cbeb9be5cd4550db79d35e3b075ac8c1b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `emqx:4.4.2` - linux; amd64

```console
$ docker pull emqx@sha256:d86d9ec27e7d8c28a6e582eddb7e495a5110f345786c98633440a2a8f8f6e40b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124618169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ef1420603b2b042c1a4a2afd1227557c6ea3e7045cd0a8e0b1c301b4335981`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 07:16:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 07:16:43 GMT
ENV EMQX_VERSION=4.4.2
# Wed, 20 Apr 2022 07:16:44 GMT
ENV OTP=otp24.1.5-3
# Wed, 20 Apr 2022 07:16:49 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="bbeb72effcbebab56a3331bdd51dbf5810121d9b2bc57a294d49e97bd9eed7f4"; fi;     if [ ${arch} = "arm64" ]; then sha256="13f6bc6b218f837bb8e7353e5470190152a8c8e19780762ad7fd0c828ef6fb29"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 20 Apr 2022 07:16:54 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 20 Apr 2022 07:16:54 GMT
WORKDIR /opt/emqx
# Wed, 20 Apr 2022 07:16:54 GMT
USER emqx
# Wed, 20 Apr 2022 07:16:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 20 Apr 2022 07:16:54 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 20 Apr 2022 07:16:55 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 20 Apr 2022 07:16:55 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 20 Apr 2022 07:16:55 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a7fa618b3ee98f630ea5fd88bb7bb8b5d6b598c968835215a4c82e3c4cfd4a`  
		Last Modified: Wed, 20 Apr 2022 07:17:22 GMT  
		Size: 2.6 MB (2568085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbceec71e45d6c2b8076974751b5d7f7cfbc56a3de4ca8a914b16bc934c6c62`  
		Last Modified: Wed, 20 Apr 2022 07:17:26 GMT  
		Size: 45.3 MB (45333518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52371626cb7e99f7c6aaebe4553506b25ee848e8bfea4449609181137cd8908d`  
		Last Modified: Wed, 20 Apr 2022 07:17:26 GMT  
		Size: 45.3 MB (45336481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71835fed0df86c8bfa5377adb33e8a60cc98830ed7d3b2a60a377b60ce27b007`  
		Last Modified: Wed, 20 Apr 2022 07:17:21 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:e20e773149bd3e95781cf87409b93cbeb9be5cd4550db79d35e3b075ac8c1b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:d86d9ec27e7d8c28a6e582eddb7e495a5110f345786c98633440a2a8f8f6e40b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124618169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ef1420603b2b042c1a4a2afd1227557c6ea3e7045cd0a8e0b1c301b4335981`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 07:16:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 07:16:43 GMT
ENV EMQX_VERSION=4.4.2
# Wed, 20 Apr 2022 07:16:44 GMT
ENV OTP=otp24.1.5-3
# Wed, 20 Apr 2022 07:16:49 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="bbeb72effcbebab56a3331bdd51dbf5810121d9b2bc57a294d49e97bd9eed7f4"; fi;     if [ ${arch} = "arm64" ]; then sha256="13f6bc6b218f837bb8e7353e5470190152a8c8e19780762ad7fd0c828ef6fb29"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 20 Apr 2022 07:16:54 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 20 Apr 2022 07:16:54 GMT
WORKDIR /opt/emqx
# Wed, 20 Apr 2022 07:16:54 GMT
USER emqx
# Wed, 20 Apr 2022 07:16:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 20 Apr 2022 07:16:54 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 20 Apr 2022 07:16:55 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 20 Apr 2022 07:16:55 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 20 Apr 2022 07:16:55 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a7fa618b3ee98f630ea5fd88bb7bb8b5d6b598c968835215a4c82e3c4cfd4a`  
		Last Modified: Wed, 20 Apr 2022 07:17:22 GMT  
		Size: 2.6 MB (2568085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbceec71e45d6c2b8076974751b5d7f7cfbc56a3de4ca8a914b16bc934c6c62`  
		Last Modified: Wed, 20 Apr 2022 07:17:26 GMT  
		Size: 45.3 MB (45333518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52371626cb7e99f7c6aaebe4553506b25ee848e8bfea4449609181137cd8908d`  
		Last Modified: Wed, 20 Apr 2022 07:17:26 GMT  
		Size: 45.3 MB (45336481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71835fed0df86c8bfa5377adb33e8a60cc98830ed7d3b2a60a377b60ce27b007`  
		Last Modified: Wed, 20 Apr 2022 07:17:21 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
