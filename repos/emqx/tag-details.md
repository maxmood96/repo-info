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
$ docker pull emqx@sha256:deb49159b8f96acb2c51fab1dcd7dce4d0075e087a88a7a5e6583b6ffe195d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:8f6588ec839454e85c7088ebca582e9c79931c0a0e2be5de0785b926e356697f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124852615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e49fad68276031992915c490219747f207413b6ea562c7275628261449c812`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:59:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:59:59 GMT
ENV EMQX_VERSION=4.4.4
# Wed, 05 Oct 2022 01:59:59 GMT
ENV OTP=otp24.1.5-3
# Wed, 05 Oct 2022 02:00:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 05 Oct 2022 02:00:10 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 05 Oct 2022 02:00:10 GMT
WORKDIR /opt/emqx
# Wed, 05 Oct 2022 02:00:10 GMT
USER emqx
# Wed, 05 Oct 2022 02:00:10 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 05 Oct 2022 02:00:10 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 05 Oct 2022 02:00:10 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 05 Oct 2022 02:00:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 02:00:11 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe095a4000e416a4a962d9e528d50c8497d6f447edeb1dca129322f95aa5e8c`  
		Last Modified: Wed, 05 Oct 2022 02:00:38 GMT  
		Size: 2.6 MB (2569549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ca5365971083f2523aace68964b85626fc613bac6ce0ecae9295ba93ea831a`  
		Last Modified: Wed, 05 Oct 2022 02:00:43 GMT  
		Size: 45.4 MB (45424513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2ffbd0d4cd94ef8244a6bfb9c4f097fa8085cf516b3661e9cb27d34d60e8e3`  
		Last Modified: Wed, 05 Oct 2022 02:00:43 GMT  
		Size: 45.4 MB (45437342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953f151a9c84e239b25e7c4076d976eb601c1a16aefb2bd7490036184be0f971`  
		Last Modified: Wed, 05 Oct 2022 02:00:38 GMT  
		Size: 1.1 KB (1109 bytes)  
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
$ docker pull emqx@sha256:2b7d7b652313910460e77f36c1e5263542d454dad5373f53b75b69b7c6f582d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.3` - linux; amd64

```console
$ docker pull emqx@sha256:b3a78f72141d51c2385fead70eb07fd3e3ed4afbbe9d98b9c5f02f7c26be0ad6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103862391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e927caf2621dac64a28b5d4a3d87e6d426ac2298ebcc1a21c63d2f4ef3444b22`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:59:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:59:40 GMT
ENV EMQX_VERSION=4.3.15
# Wed, 05 Oct 2022 01:59:44 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 05 Oct 2022 01:59:50 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 05 Oct 2022 01:59:50 GMT
WORKDIR /opt/emqx
# Wed, 05 Oct 2022 01:59:50 GMT
USER emqx
# Wed, 05 Oct 2022 01:59:50 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 05 Oct 2022 01:59:50 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 05 Oct 2022 01:59:51 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Wed, 05 Oct 2022 01:59:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 01:59:51 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d7e8746e5824bcc8ef2e6b31fff84d7e291f2e06df4fcd676841851c6be797`  
		Last Modified: Wed, 05 Oct 2022 02:00:24 GMT  
		Size: 4.6 MB (4610492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db704871a9c9e6194193a4ed37671ba63d657da44ecee6322fafb29011fde6d2`  
		Last Modified: Wed, 05 Oct 2022 02:00:28 GMT  
		Size: 36.1 MB (36056920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d3de790bf6ce29aa3a2d30f630e5191ee9560229c029417dd553d396cbfeb3`  
		Last Modified: Wed, 05 Oct 2022 02:00:28 GMT  
		Size: 36.1 MB (36055894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f47921a86c7593978d05b4849b5b2e55d4da4bcc65c54d6df601e19b0a82ce3`  
		Last Modified: Wed, 05 Oct 2022 02:00:23 GMT  
		Size: 1.0 KB (1042 bytes)  
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
$ docker pull emqx@sha256:2b7d7b652313910460e77f36c1e5263542d454dad5373f53b75b69b7c6f582d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.3.15` - linux; amd64

```console
$ docker pull emqx@sha256:b3a78f72141d51c2385fead70eb07fd3e3ed4afbbe9d98b9c5f02f7c26be0ad6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103862391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e927caf2621dac64a28b5d4a3d87e6d426ac2298ebcc1a21c63d2f4ef3444b22`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:59:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:59:40 GMT
ENV EMQX_VERSION=4.3.15
# Wed, 05 Oct 2022 01:59:44 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 05 Oct 2022 01:59:50 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 05 Oct 2022 01:59:50 GMT
WORKDIR /opt/emqx
# Wed, 05 Oct 2022 01:59:50 GMT
USER emqx
# Wed, 05 Oct 2022 01:59:50 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 05 Oct 2022 01:59:50 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 05 Oct 2022 01:59:51 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Wed, 05 Oct 2022 01:59:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 01:59:51 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d7e8746e5824bcc8ef2e6b31fff84d7e291f2e06df4fcd676841851c6be797`  
		Last Modified: Wed, 05 Oct 2022 02:00:24 GMT  
		Size: 4.6 MB (4610492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db704871a9c9e6194193a4ed37671ba63d657da44ecee6322fafb29011fde6d2`  
		Last Modified: Wed, 05 Oct 2022 02:00:28 GMT  
		Size: 36.1 MB (36056920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d3de790bf6ce29aa3a2d30f630e5191ee9560229c029417dd553d396cbfeb3`  
		Last Modified: Wed, 05 Oct 2022 02:00:28 GMT  
		Size: 36.1 MB (36055894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f47921a86c7593978d05b4849b5b2e55d4da4bcc65c54d6df601e19b0a82ce3`  
		Last Modified: Wed, 05 Oct 2022 02:00:23 GMT  
		Size: 1.0 KB (1042 bytes)  
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
$ docker pull emqx@sha256:deb49159b8f96acb2c51fab1dcd7dce4d0075e087a88a7a5e6583b6ffe195d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:8f6588ec839454e85c7088ebca582e9c79931c0a0e2be5de0785b926e356697f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124852615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e49fad68276031992915c490219747f207413b6ea562c7275628261449c812`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:59:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:59:59 GMT
ENV EMQX_VERSION=4.4.4
# Wed, 05 Oct 2022 01:59:59 GMT
ENV OTP=otp24.1.5-3
# Wed, 05 Oct 2022 02:00:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 05 Oct 2022 02:00:10 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 05 Oct 2022 02:00:10 GMT
WORKDIR /opt/emqx
# Wed, 05 Oct 2022 02:00:10 GMT
USER emqx
# Wed, 05 Oct 2022 02:00:10 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 05 Oct 2022 02:00:10 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 05 Oct 2022 02:00:10 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 05 Oct 2022 02:00:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 02:00:11 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe095a4000e416a4a962d9e528d50c8497d6f447edeb1dca129322f95aa5e8c`  
		Last Modified: Wed, 05 Oct 2022 02:00:38 GMT  
		Size: 2.6 MB (2569549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ca5365971083f2523aace68964b85626fc613bac6ce0ecae9295ba93ea831a`  
		Last Modified: Wed, 05 Oct 2022 02:00:43 GMT  
		Size: 45.4 MB (45424513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2ffbd0d4cd94ef8244a6bfb9c4f097fa8085cf516b3661e9cb27d34d60e8e3`  
		Last Modified: Wed, 05 Oct 2022 02:00:43 GMT  
		Size: 45.4 MB (45437342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953f151a9c84e239b25e7c4076d976eb601c1a16aefb2bd7490036184be0f971`  
		Last Modified: Wed, 05 Oct 2022 02:00:38 GMT  
		Size: 1.1 KB (1109 bytes)  
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
$ docker pull emqx@sha256:deb49159b8f96acb2c51fab1dcd7dce4d0075e087a88a7a5e6583b6ffe195d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4.4` - linux; amd64

```console
$ docker pull emqx@sha256:8f6588ec839454e85c7088ebca582e9c79931c0a0e2be5de0785b926e356697f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124852615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e49fad68276031992915c490219747f207413b6ea562c7275628261449c812`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:59:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:59:59 GMT
ENV EMQX_VERSION=4.4.4
# Wed, 05 Oct 2022 01:59:59 GMT
ENV OTP=otp24.1.5-3
# Wed, 05 Oct 2022 02:00:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 05 Oct 2022 02:00:10 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 05 Oct 2022 02:00:10 GMT
WORKDIR /opt/emqx
# Wed, 05 Oct 2022 02:00:10 GMT
USER emqx
# Wed, 05 Oct 2022 02:00:10 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 05 Oct 2022 02:00:10 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 05 Oct 2022 02:00:10 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 05 Oct 2022 02:00:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 02:00:11 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe095a4000e416a4a962d9e528d50c8497d6f447edeb1dca129322f95aa5e8c`  
		Last Modified: Wed, 05 Oct 2022 02:00:38 GMT  
		Size: 2.6 MB (2569549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ca5365971083f2523aace68964b85626fc613bac6ce0ecae9295ba93ea831a`  
		Last Modified: Wed, 05 Oct 2022 02:00:43 GMT  
		Size: 45.4 MB (45424513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2ffbd0d4cd94ef8244a6bfb9c4f097fa8085cf516b3661e9cb27d34d60e8e3`  
		Last Modified: Wed, 05 Oct 2022 02:00:43 GMT  
		Size: 45.4 MB (45437342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953f151a9c84e239b25e7c4076d976eb601c1a16aefb2bd7490036184be0f971`  
		Last Modified: Wed, 05 Oct 2022 02:00:38 GMT  
		Size: 1.1 KB (1109 bytes)  
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
$ docker pull emqx@sha256:deb49159b8f96acb2c51fab1dcd7dce4d0075e087a88a7a5e6583b6ffe195d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:8f6588ec839454e85c7088ebca582e9c79931c0a0e2be5de0785b926e356697f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124852615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e49fad68276031992915c490219747f207413b6ea562c7275628261449c812`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:59:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:59:59 GMT
ENV EMQX_VERSION=4.4.4
# Wed, 05 Oct 2022 01:59:59 GMT
ENV OTP=otp24.1.5-3
# Wed, 05 Oct 2022 02:00:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 05 Oct 2022 02:00:10 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 05 Oct 2022 02:00:10 GMT
WORKDIR /opt/emqx
# Wed, 05 Oct 2022 02:00:10 GMT
USER emqx
# Wed, 05 Oct 2022 02:00:10 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 05 Oct 2022 02:00:10 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 05 Oct 2022 02:00:10 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 05 Oct 2022 02:00:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 02:00:11 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe095a4000e416a4a962d9e528d50c8497d6f447edeb1dca129322f95aa5e8c`  
		Last Modified: Wed, 05 Oct 2022 02:00:38 GMT  
		Size: 2.6 MB (2569549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ca5365971083f2523aace68964b85626fc613bac6ce0ecae9295ba93ea831a`  
		Last Modified: Wed, 05 Oct 2022 02:00:43 GMT  
		Size: 45.4 MB (45424513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2ffbd0d4cd94ef8244a6bfb9c4f097fa8085cf516b3661e9cb27d34d60e8e3`  
		Last Modified: Wed, 05 Oct 2022 02:00:43 GMT  
		Size: 45.4 MB (45437342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953f151a9c84e239b25e7c4076d976eb601c1a16aefb2bd7490036184be0f971`  
		Last Modified: Wed, 05 Oct 2022 02:00:38 GMT  
		Size: 1.1 KB (1109 bytes)  
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
