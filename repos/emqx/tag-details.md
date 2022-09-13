<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:4`](#emqx4)
-	[`emqx:4.3`](#emqx43)
-	[`emqx:4.3.15`](#emqx4315)
-	[`emqx:4.4`](#emqx44)
-	[`emqx:4.4.4`](#emqx444)
-	[`emqx:latest`](#emqxlatest)

## `emqx:4`

```console
$ docker pull emqx@sha256:1463a7e55f99a015fc767c798979a360ad9f4e874fbced66ecc3c2ef7a0f4f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:fb2257b976208201d7e33177427e0be10a94168dfc39bb257de940e3e339317c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124836587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f34e0da055730b616341cff9eecc144f26b5d0df9a5c84e0d83c6957bed4ed`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:59:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:59:23 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 13 Sep 2022 03:59:23 GMT
ENV OTP=otp24.1.5-3
# Tue, 13 Sep 2022 03:59:27 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Sep 2022 03:59:33 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 13 Sep 2022 03:59:33 GMT
WORKDIR /opt/emqx
# Tue, 13 Sep 2022 03:59:33 GMT
USER emqx
# Tue, 13 Sep 2022 03:59:33 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Sep 2022 03:59:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Sep 2022 03:59:34 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 13 Sep 2022 03:59:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:59:34 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1718cfc9ab1a66a45b214f22aad7acd47b0ee5360a06535c5c7108a46fbee1`  
		Last Modified: Tue, 13 Sep 2022 04:00:04 GMT  
		Size: 2.6 MB (2569503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9004193e42b45379e1def33644c4824ac57de3e65880a3316bb03d535de9fb`  
		Last Modified: Tue, 13 Sep 2022 04:00:08 GMT  
		Size: 45.4 MB (45424530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e1552a0b575c61fc3b386fa2dccef591129271e5914cec5e588908f4e26418`  
		Last Modified: Tue, 13 Sep 2022 04:00:08 GMT  
		Size: 45.4 MB (45437326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dd750521fd7780e66dac97a3c8dc8ff81efc749ccf491617bdde85021e3dee`  
		Last Modified: Tue, 13 Sep 2022 04:00:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:e4f6ef153763cbddda8d7a0972a63966a2abd4fafe0ff4759031a2600756254a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110228391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccaed5f3197d958174b58814ad1547d68d0d1e629713c8eb7a28f290d9047601`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 05:17:06 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 05:17:06 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 13 Sep 2022 05:17:07 GMT
ENV OTP=otp24.1.5-3
# Tue, 13 Sep 2022 05:17:12 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Sep 2022 05:17:13 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 13 Sep 2022 05:17:13 GMT
WORKDIR /opt/emqx
# Tue, 13 Sep 2022 05:17:14 GMT
USER emqx
# Tue, 13 Sep 2022 05:17:15 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Sep 2022 05:17:16 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Sep 2022 05:17:18 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 13 Sep 2022 05:17:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 05:17:19 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77e5f9db574c8e5defbcd48a44918faa2f2842d9bd85dedf9b48af55e6ec4d7`  
		Last Modified: Tue, 13 Sep 2022 05:17:57 GMT  
		Size: 2.6 MB (2558536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469fe8caece04ec435842d67386bab1840a0a4d7261acb37f28ed7b78eb32537`  
		Last Modified: Tue, 13 Sep 2022 05:18:01 GMT  
		Size: 38.8 MB (38806756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57217c8e8e7bc3008a73ee8e731ab3e208549ce64d5d067f021fb4b3694c52e0`  
		Last Modified: Tue, 13 Sep 2022 05:18:01 GMT  
		Size: 38.8 MB (38807751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c436c7e55b55026c991806cb2c4b07fc46ab24aab1d955b7205f9377371b18`  
		Last Modified: Tue, 13 Sep 2022 05:17:56 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3`

```console
$ docker pull emqx@sha256:9b5b319e25190a93fc5dc973370891c13df2eafaae63d3997578671a64d2eaec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.3` - linux; amd64

```console
$ docker pull emqx@sha256:32c4518a52c03e9d829291167d34d19874eadea0abe85e9d1b2ef00aa2d35f9b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103855150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51febc65abc7cc401b23f068a0bc6a1d7de5c07b275bcbf54828f0a0208f4578`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:59:04 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:59:04 GMT
ENV EMQX_VERSION=4.3.15
# Tue, 13 Sep 2022 03:59:08 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Sep 2022 03:59:13 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 13 Sep 2022 03:59:14 GMT
WORKDIR /opt/emqx
# Tue, 13 Sep 2022 03:59:14 GMT
USER emqx
# Tue, 13 Sep 2022 03:59:14 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Sep 2022 03:59:14 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Sep 2022 03:59:14 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 13 Sep 2022 03:59:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:59:14 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76cceb548f828bd9213a8cdc23f9bfaa531c7f1d73ccabbdfaadce43a352c0e0`  
		Last Modified: Tue, 13 Sep 2022 03:59:49 GMT  
		Size: 4.6 MB (4610632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07eca7a7df10e3eb8a591f9a51d6f53034b529d3dfa6ffc056fdbce0dcaff11`  
		Last Modified: Tue, 13 Sep 2022 03:59:53 GMT  
		Size: 36.1 MB (36056967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00867241da64c428bcc94c253fff65bfc0df3bd1bc7c4c38be22ac90db7dd957`  
		Last Modified: Tue, 13 Sep 2022 03:59:53 GMT  
		Size: 36.1 MB (36055960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba36560a74cdb0c834d5c092cee7c1b2a59f000b123d092237951250e0a973e7`  
		Last Modified: Tue, 13 Sep 2022 03:59:48 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:5926776d57170dd3ab6c8e3ecfe6a343f71ee99c05420cdde0764231afe15969
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101926571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f8476a2159d3bdd62b08e77f0a5a7f693c10fa1f9f31521497d022052ddb56`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 13 Sep 2022 02:11:20 GMT
ADD file:18fa3591fcbf0c3e065dbe581a069fc2af6fab9e4446047348404881af960725 in / 
# Tue, 13 Sep 2022 02:11:21 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 05:16:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 05:16:41 GMT
ENV EMQX_VERSION=4.3.15
# Tue, 13 Sep 2022 05:16:47 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Sep 2022 05:16:49 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 13 Sep 2022 05:16:49 GMT
WORKDIR /opt/emqx
# Tue, 13 Sep 2022 05:16:50 GMT
USER emqx
# Tue, 13 Sep 2022 05:16:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Sep 2022 05:16:52 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Sep 2022 05:16:54 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 13 Sep 2022 05:16:54 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 05:16:55 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:4c3f5cce277263c7aeaf67f83255af76927e03363e775f39d7587bc5036fcf1e`  
		Last Modified: Tue, 13 Sep 2022 02:17:10 GMT  
		Size: 25.9 MB (25904152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dae122871f94f58da97cea58bbcc2560398fe72b9566886528ed5d0dadb26af`  
		Last Modified: Tue, 13 Sep 2022 05:17:42 GMT  
		Size: 4.5 MB (4486389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734202560d2527689c5fa3d45f8fdab90cca6709a176bc5b9809330d4062e9cb`  
		Last Modified: Tue, 13 Sep 2022 05:17:45 GMT  
		Size: 35.8 MB (35761671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea818cb02df9f0c270cff6c01b41b1e5b1186c10f9c6aa315d3cd8f58442505a`  
		Last Modified: Tue, 13 Sep 2022 05:17:45 GMT  
		Size: 35.8 MB (35773317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82023f8ee59ca7a1799e4f0e52809756ad033a00310481006a3f16aa7d420d7b`  
		Last Modified: Tue, 13 Sep 2022 05:17:41 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3.15`

```console
$ docker pull emqx@sha256:9b5b319e25190a93fc5dc973370891c13df2eafaae63d3997578671a64d2eaec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.3.15` - linux; amd64

```console
$ docker pull emqx@sha256:32c4518a52c03e9d829291167d34d19874eadea0abe85e9d1b2ef00aa2d35f9b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103855150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51febc65abc7cc401b23f068a0bc6a1d7de5c07b275bcbf54828f0a0208f4578`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:59:04 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:59:04 GMT
ENV EMQX_VERSION=4.3.15
# Tue, 13 Sep 2022 03:59:08 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Sep 2022 03:59:13 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 13 Sep 2022 03:59:14 GMT
WORKDIR /opt/emqx
# Tue, 13 Sep 2022 03:59:14 GMT
USER emqx
# Tue, 13 Sep 2022 03:59:14 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Sep 2022 03:59:14 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Sep 2022 03:59:14 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 13 Sep 2022 03:59:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:59:14 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76cceb548f828bd9213a8cdc23f9bfaa531c7f1d73ccabbdfaadce43a352c0e0`  
		Last Modified: Tue, 13 Sep 2022 03:59:49 GMT  
		Size: 4.6 MB (4610632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07eca7a7df10e3eb8a591f9a51d6f53034b529d3dfa6ffc056fdbce0dcaff11`  
		Last Modified: Tue, 13 Sep 2022 03:59:53 GMT  
		Size: 36.1 MB (36056967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00867241da64c428bcc94c253fff65bfc0df3bd1bc7c4c38be22ac90db7dd957`  
		Last Modified: Tue, 13 Sep 2022 03:59:53 GMT  
		Size: 36.1 MB (36055960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba36560a74cdb0c834d5c092cee7c1b2a59f000b123d092237951250e0a973e7`  
		Last Modified: Tue, 13 Sep 2022 03:59:48 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.3.15` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:5926776d57170dd3ab6c8e3ecfe6a343f71ee99c05420cdde0764231afe15969
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101926571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f8476a2159d3bdd62b08e77f0a5a7f693c10fa1f9f31521497d022052ddb56`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 13 Sep 2022 02:11:20 GMT
ADD file:18fa3591fcbf0c3e065dbe581a069fc2af6fab9e4446047348404881af960725 in / 
# Tue, 13 Sep 2022 02:11:21 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 05:16:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 05:16:41 GMT
ENV EMQX_VERSION=4.3.15
# Tue, 13 Sep 2022 05:16:47 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Sep 2022 05:16:49 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 13 Sep 2022 05:16:49 GMT
WORKDIR /opt/emqx
# Tue, 13 Sep 2022 05:16:50 GMT
USER emqx
# Tue, 13 Sep 2022 05:16:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Sep 2022 05:16:52 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Sep 2022 05:16:54 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 13 Sep 2022 05:16:54 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 05:16:55 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:4c3f5cce277263c7aeaf67f83255af76927e03363e775f39d7587bc5036fcf1e`  
		Last Modified: Tue, 13 Sep 2022 02:17:10 GMT  
		Size: 25.9 MB (25904152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dae122871f94f58da97cea58bbcc2560398fe72b9566886528ed5d0dadb26af`  
		Last Modified: Tue, 13 Sep 2022 05:17:42 GMT  
		Size: 4.5 MB (4486389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734202560d2527689c5fa3d45f8fdab90cca6709a176bc5b9809330d4062e9cb`  
		Last Modified: Tue, 13 Sep 2022 05:17:45 GMT  
		Size: 35.8 MB (35761671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea818cb02df9f0c270cff6c01b41b1e5b1186c10f9c6aa315d3cd8f58442505a`  
		Last Modified: Tue, 13 Sep 2022 05:17:45 GMT  
		Size: 35.8 MB (35773317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82023f8ee59ca7a1799e4f0e52809756ad033a00310481006a3f16aa7d420d7b`  
		Last Modified: Tue, 13 Sep 2022 05:17:41 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:1463a7e55f99a015fc767c798979a360ad9f4e874fbced66ecc3c2ef7a0f4f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:fb2257b976208201d7e33177427e0be10a94168dfc39bb257de940e3e339317c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124836587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f34e0da055730b616341cff9eecc144f26b5d0df9a5c84e0d83c6957bed4ed`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:59:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:59:23 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 13 Sep 2022 03:59:23 GMT
ENV OTP=otp24.1.5-3
# Tue, 13 Sep 2022 03:59:27 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Sep 2022 03:59:33 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 13 Sep 2022 03:59:33 GMT
WORKDIR /opt/emqx
# Tue, 13 Sep 2022 03:59:33 GMT
USER emqx
# Tue, 13 Sep 2022 03:59:33 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Sep 2022 03:59:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Sep 2022 03:59:34 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 13 Sep 2022 03:59:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:59:34 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1718cfc9ab1a66a45b214f22aad7acd47b0ee5360a06535c5c7108a46fbee1`  
		Last Modified: Tue, 13 Sep 2022 04:00:04 GMT  
		Size: 2.6 MB (2569503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9004193e42b45379e1def33644c4824ac57de3e65880a3316bb03d535de9fb`  
		Last Modified: Tue, 13 Sep 2022 04:00:08 GMT  
		Size: 45.4 MB (45424530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e1552a0b575c61fc3b386fa2dccef591129271e5914cec5e588908f4e26418`  
		Last Modified: Tue, 13 Sep 2022 04:00:08 GMT  
		Size: 45.4 MB (45437326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dd750521fd7780e66dac97a3c8dc8ff81efc749ccf491617bdde85021e3dee`  
		Last Modified: Tue, 13 Sep 2022 04:00:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:e4f6ef153763cbddda8d7a0972a63966a2abd4fafe0ff4759031a2600756254a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110228391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccaed5f3197d958174b58814ad1547d68d0d1e629713c8eb7a28f290d9047601`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 05:17:06 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 05:17:06 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 13 Sep 2022 05:17:07 GMT
ENV OTP=otp24.1.5-3
# Tue, 13 Sep 2022 05:17:12 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Sep 2022 05:17:13 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 13 Sep 2022 05:17:13 GMT
WORKDIR /opt/emqx
# Tue, 13 Sep 2022 05:17:14 GMT
USER emqx
# Tue, 13 Sep 2022 05:17:15 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Sep 2022 05:17:16 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Sep 2022 05:17:18 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 13 Sep 2022 05:17:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 05:17:19 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77e5f9db574c8e5defbcd48a44918faa2f2842d9bd85dedf9b48af55e6ec4d7`  
		Last Modified: Tue, 13 Sep 2022 05:17:57 GMT  
		Size: 2.6 MB (2558536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469fe8caece04ec435842d67386bab1840a0a4d7261acb37f28ed7b78eb32537`  
		Last Modified: Tue, 13 Sep 2022 05:18:01 GMT  
		Size: 38.8 MB (38806756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57217c8e8e7bc3008a73ee8e731ab3e208549ce64d5d067f021fb4b3694c52e0`  
		Last Modified: Tue, 13 Sep 2022 05:18:01 GMT  
		Size: 38.8 MB (38807751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c436c7e55b55026c991806cb2c4b07fc46ab24aab1d955b7205f9377371b18`  
		Last Modified: Tue, 13 Sep 2022 05:17:56 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.4`

```console
$ docker pull emqx@sha256:1463a7e55f99a015fc767c798979a360ad9f4e874fbced66ecc3c2ef7a0f4f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4.4` - linux; amd64

```console
$ docker pull emqx@sha256:fb2257b976208201d7e33177427e0be10a94168dfc39bb257de940e3e339317c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124836587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f34e0da055730b616341cff9eecc144f26b5d0df9a5c84e0d83c6957bed4ed`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:59:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:59:23 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 13 Sep 2022 03:59:23 GMT
ENV OTP=otp24.1.5-3
# Tue, 13 Sep 2022 03:59:27 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Sep 2022 03:59:33 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 13 Sep 2022 03:59:33 GMT
WORKDIR /opt/emqx
# Tue, 13 Sep 2022 03:59:33 GMT
USER emqx
# Tue, 13 Sep 2022 03:59:33 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Sep 2022 03:59:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Sep 2022 03:59:34 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 13 Sep 2022 03:59:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:59:34 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1718cfc9ab1a66a45b214f22aad7acd47b0ee5360a06535c5c7108a46fbee1`  
		Last Modified: Tue, 13 Sep 2022 04:00:04 GMT  
		Size: 2.6 MB (2569503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9004193e42b45379e1def33644c4824ac57de3e65880a3316bb03d535de9fb`  
		Last Modified: Tue, 13 Sep 2022 04:00:08 GMT  
		Size: 45.4 MB (45424530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e1552a0b575c61fc3b386fa2dccef591129271e5914cec5e588908f4e26418`  
		Last Modified: Tue, 13 Sep 2022 04:00:08 GMT  
		Size: 45.4 MB (45437326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dd750521fd7780e66dac97a3c8dc8ff81efc749ccf491617bdde85021e3dee`  
		Last Modified: Tue, 13 Sep 2022 04:00:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:e4f6ef153763cbddda8d7a0972a63966a2abd4fafe0ff4759031a2600756254a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110228391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccaed5f3197d958174b58814ad1547d68d0d1e629713c8eb7a28f290d9047601`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 05:17:06 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 05:17:06 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 13 Sep 2022 05:17:07 GMT
ENV OTP=otp24.1.5-3
# Tue, 13 Sep 2022 05:17:12 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Sep 2022 05:17:13 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 13 Sep 2022 05:17:13 GMT
WORKDIR /opt/emqx
# Tue, 13 Sep 2022 05:17:14 GMT
USER emqx
# Tue, 13 Sep 2022 05:17:15 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Sep 2022 05:17:16 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Sep 2022 05:17:18 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 13 Sep 2022 05:17:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 05:17:19 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77e5f9db574c8e5defbcd48a44918faa2f2842d9bd85dedf9b48af55e6ec4d7`  
		Last Modified: Tue, 13 Sep 2022 05:17:57 GMT  
		Size: 2.6 MB (2558536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469fe8caece04ec435842d67386bab1840a0a4d7261acb37f28ed7b78eb32537`  
		Last Modified: Tue, 13 Sep 2022 05:18:01 GMT  
		Size: 38.8 MB (38806756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57217c8e8e7bc3008a73ee8e731ab3e208549ce64d5d067f021fb4b3694c52e0`  
		Last Modified: Tue, 13 Sep 2022 05:18:01 GMT  
		Size: 38.8 MB (38807751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c436c7e55b55026c991806cb2c4b07fc46ab24aab1d955b7205f9377371b18`  
		Last Modified: Tue, 13 Sep 2022 05:17:56 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:1463a7e55f99a015fc767c798979a360ad9f4e874fbced66ecc3c2ef7a0f4f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:fb2257b976208201d7e33177427e0be10a94168dfc39bb257de940e3e339317c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124836587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f34e0da055730b616341cff9eecc144f26b5d0df9a5c84e0d83c6957bed4ed`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:59:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:59:23 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 13 Sep 2022 03:59:23 GMT
ENV OTP=otp24.1.5-3
# Tue, 13 Sep 2022 03:59:27 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Sep 2022 03:59:33 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 13 Sep 2022 03:59:33 GMT
WORKDIR /opt/emqx
# Tue, 13 Sep 2022 03:59:33 GMT
USER emqx
# Tue, 13 Sep 2022 03:59:33 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Sep 2022 03:59:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Sep 2022 03:59:34 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 13 Sep 2022 03:59:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:59:34 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1718cfc9ab1a66a45b214f22aad7acd47b0ee5360a06535c5c7108a46fbee1`  
		Last Modified: Tue, 13 Sep 2022 04:00:04 GMT  
		Size: 2.6 MB (2569503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9004193e42b45379e1def33644c4824ac57de3e65880a3316bb03d535de9fb`  
		Last Modified: Tue, 13 Sep 2022 04:00:08 GMT  
		Size: 45.4 MB (45424530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e1552a0b575c61fc3b386fa2dccef591129271e5914cec5e588908f4e26418`  
		Last Modified: Tue, 13 Sep 2022 04:00:08 GMT  
		Size: 45.4 MB (45437326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dd750521fd7780e66dac97a3c8dc8ff81efc749ccf491617bdde85021e3dee`  
		Last Modified: Tue, 13 Sep 2022 04:00:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:e4f6ef153763cbddda8d7a0972a63966a2abd4fafe0ff4759031a2600756254a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110228391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccaed5f3197d958174b58814ad1547d68d0d1e629713c8eb7a28f290d9047601`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 05:17:06 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 05:17:06 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 13 Sep 2022 05:17:07 GMT
ENV OTP=otp24.1.5-3
# Tue, 13 Sep 2022 05:17:12 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Sep 2022 05:17:13 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 13 Sep 2022 05:17:13 GMT
WORKDIR /opt/emqx
# Tue, 13 Sep 2022 05:17:14 GMT
USER emqx
# Tue, 13 Sep 2022 05:17:15 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Sep 2022 05:17:16 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Sep 2022 05:17:18 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 13 Sep 2022 05:17:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 05:17:19 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77e5f9db574c8e5defbcd48a44918faa2f2842d9bd85dedf9b48af55e6ec4d7`  
		Last Modified: Tue, 13 Sep 2022 05:17:57 GMT  
		Size: 2.6 MB (2558536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469fe8caece04ec435842d67386bab1840a0a4d7261acb37f28ed7b78eb32537`  
		Last Modified: Tue, 13 Sep 2022 05:18:01 GMT  
		Size: 38.8 MB (38806756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57217c8e8e7bc3008a73ee8e731ab3e208549ce64d5d067f021fb4b3694c52e0`  
		Last Modified: Tue, 13 Sep 2022 05:18:01 GMT  
		Size: 38.8 MB (38807751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c436c7e55b55026c991806cb2c4b07fc46ab24aab1d955b7205f9377371b18`  
		Last Modified: Tue, 13 Sep 2022 05:17:56 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
