<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:4`](#emqx4)
-	[`emqx:4.4`](#emqx44)
-	[`emqx:4.4.16`](#emqx4416)
-	[`emqx:5`](#emqx5)
-	[`emqx:5.0`](#emqx50)
-	[`emqx:5.0.20`](#emqx5020)
-	[`emqx:latest`](#emqxlatest)

## `emqx:4`

```console
$ docker pull emqx@sha256:7d65f058645c9d9b9dbb9645333ebf720d06671ee752f530bb0f649e326f3785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:f3b580bdf06cf3dd7e60bf894a6c125cf55b29cd1723b9ec35e2f0b16063ac28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81272303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c7411cbf93ac1c8d1476644d0ceb049e0abdbe5b656b6d3e8df6f8eac772b3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:03:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:03:11 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 15 Mar 2023 23:28:17 GMT
ENV EMQX_VERSION=4.4.16
# Wed, 15 Mar 2023 23:28:17 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 15 Mar 2023 23:28:21 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="901b76ea2bee68729b75280740ca31b1af5b358d331422d1653dc342ee830324"; fi;     if [ ${arch} = "arm64" ]; then sha256="1224f53d0ee98390c286f3bbd9af2f294c2fa4ccb79342343d803fa234165c6e"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 15 Mar 2023 23:28:21 GMT
WORKDIR /opt/emqx
# Wed, 15 Mar 2023 23:28:22 GMT
USER emqx
# Wed, 15 Mar 2023 23:28:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 15 Mar 2023 23:28:22 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 15 Mar 2023 23:28:22 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 15 Mar 2023 23:28:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 15 Mar 2023 23:28:22 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396ee3d6a271f9fce1d0b1fd4fc0bd3a54cd9c9139a819de5351b130046fea9d`  
		Last Modified: Wed, 01 Mar 2023 05:04:03 GMT  
		Size: 2.6 MB (2569541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79aa88ad721c3aad2bd0e2aaccdbb555263a96f1e69f9f9e7e2e698cbd61acf`  
		Last Modified: Wed, 01 Mar 2023 05:04:02 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8943a0bcb1f0d0512ed4d4f6cb52cbb45f7497f16a74fda13d0ec343c375f626`  
		Last Modified: Wed, 15 Mar 2023 23:28:41 GMT  
		Size: 47.3 MB (47286141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a2b18c61a7d3a97a7493d4c03698ead2a79a6e9f45985619f41fd6df9fcc15`  
		Last Modified: Wed, 15 Mar 2023 23:28:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4e9ebe772c56e5076b7d356635a535cf5565d54c26264c0848393a3a91f757a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72700283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e4a8802d3708ed0e9e04e9eba2393ce51bc8cae915d012bf4f4374b1d66882`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:21:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 03:21:03 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 15 Mar 2023 23:40:08 GMT
ENV EMQX_VERSION=4.4.16
# Wed, 15 Mar 2023 23:40:08 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 15 Mar 2023 23:40:11 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="901b76ea2bee68729b75280740ca31b1af5b358d331422d1653dc342ee830324"; fi;     if [ ${arch} = "arm64" ]; then sha256="1224f53d0ee98390c286f3bbd9af2f294c2fa4ccb79342343d803fa234165c6e"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 15 Mar 2023 23:40:12 GMT
WORKDIR /opt/emqx
# Wed, 15 Mar 2023 23:40:12 GMT
USER emqx
# Wed, 15 Mar 2023 23:40:12 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 15 Mar 2023 23:40:12 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 15 Mar 2023 23:40:12 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 15 Mar 2023 23:40:12 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 15 Mar 2023 23:40:12 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ea117f9b26bad2c79fea1dafb19b2ccbfb0e0744061d7743a5aea0c0e38af7`  
		Last Modified: Wed, 01 Mar 2023 03:21:50 GMT  
		Size: 2.6 MB (2559230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fde159950f1c178189d5f614a5405bd1df5caabc1ebd2bfc1e35376f9bd0e19`  
		Last Modified: Wed, 01 Mar 2023 03:21:50 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4e303f3e8ae9c4c0212bb811a988e668b8fb253f34804cf455d4b4179c1ccf`  
		Last Modified: Wed, 15 Mar 2023 23:40:31 GMT  
		Size: 40.1 MB (40073017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209dd83a5db4a0f1352247f1e19e02a3a54ee87fb2e45771e96d01045483e4aa`  
		Last Modified: Wed, 15 Mar 2023 23:40:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:7d65f058645c9d9b9dbb9645333ebf720d06671ee752f530bb0f649e326f3785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:f3b580bdf06cf3dd7e60bf894a6c125cf55b29cd1723b9ec35e2f0b16063ac28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81272303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c7411cbf93ac1c8d1476644d0ceb049e0abdbe5b656b6d3e8df6f8eac772b3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:03:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:03:11 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 15 Mar 2023 23:28:17 GMT
ENV EMQX_VERSION=4.4.16
# Wed, 15 Mar 2023 23:28:17 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 15 Mar 2023 23:28:21 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="901b76ea2bee68729b75280740ca31b1af5b358d331422d1653dc342ee830324"; fi;     if [ ${arch} = "arm64" ]; then sha256="1224f53d0ee98390c286f3bbd9af2f294c2fa4ccb79342343d803fa234165c6e"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 15 Mar 2023 23:28:21 GMT
WORKDIR /opt/emqx
# Wed, 15 Mar 2023 23:28:22 GMT
USER emqx
# Wed, 15 Mar 2023 23:28:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 15 Mar 2023 23:28:22 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 15 Mar 2023 23:28:22 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 15 Mar 2023 23:28:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 15 Mar 2023 23:28:22 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396ee3d6a271f9fce1d0b1fd4fc0bd3a54cd9c9139a819de5351b130046fea9d`  
		Last Modified: Wed, 01 Mar 2023 05:04:03 GMT  
		Size: 2.6 MB (2569541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79aa88ad721c3aad2bd0e2aaccdbb555263a96f1e69f9f9e7e2e698cbd61acf`  
		Last Modified: Wed, 01 Mar 2023 05:04:02 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8943a0bcb1f0d0512ed4d4f6cb52cbb45f7497f16a74fda13d0ec343c375f626`  
		Last Modified: Wed, 15 Mar 2023 23:28:41 GMT  
		Size: 47.3 MB (47286141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a2b18c61a7d3a97a7493d4c03698ead2a79a6e9f45985619f41fd6df9fcc15`  
		Last Modified: Wed, 15 Mar 2023 23:28:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4e9ebe772c56e5076b7d356635a535cf5565d54c26264c0848393a3a91f757a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72700283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e4a8802d3708ed0e9e04e9eba2393ce51bc8cae915d012bf4f4374b1d66882`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:21:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 03:21:03 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 15 Mar 2023 23:40:08 GMT
ENV EMQX_VERSION=4.4.16
# Wed, 15 Mar 2023 23:40:08 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 15 Mar 2023 23:40:11 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="901b76ea2bee68729b75280740ca31b1af5b358d331422d1653dc342ee830324"; fi;     if [ ${arch} = "arm64" ]; then sha256="1224f53d0ee98390c286f3bbd9af2f294c2fa4ccb79342343d803fa234165c6e"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 15 Mar 2023 23:40:12 GMT
WORKDIR /opt/emqx
# Wed, 15 Mar 2023 23:40:12 GMT
USER emqx
# Wed, 15 Mar 2023 23:40:12 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 15 Mar 2023 23:40:12 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 15 Mar 2023 23:40:12 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 15 Mar 2023 23:40:12 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 15 Mar 2023 23:40:12 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ea117f9b26bad2c79fea1dafb19b2ccbfb0e0744061d7743a5aea0c0e38af7`  
		Last Modified: Wed, 01 Mar 2023 03:21:50 GMT  
		Size: 2.6 MB (2559230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fde159950f1c178189d5f614a5405bd1df5caabc1ebd2bfc1e35376f9bd0e19`  
		Last Modified: Wed, 01 Mar 2023 03:21:50 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4e303f3e8ae9c4c0212bb811a988e668b8fb253f34804cf455d4b4179c1ccf`  
		Last Modified: Wed, 15 Mar 2023 23:40:31 GMT  
		Size: 40.1 MB (40073017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209dd83a5db4a0f1352247f1e19e02a3a54ee87fb2e45771e96d01045483e4aa`  
		Last Modified: Wed, 15 Mar 2023 23:40:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.16`

```console
$ docker pull emqx@sha256:7d65f058645c9d9b9dbb9645333ebf720d06671ee752f530bb0f649e326f3785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4.16` - linux; amd64

```console
$ docker pull emqx@sha256:f3b580bdf06cf3dd7e60bf894a6c125cf55b29cd1723b9ec35e2f0b16063ac28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81272303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c7411cbf93ac1c8d1476644d0ceb049e0abdbe5b656b6d3e8df6f8eac772b3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:03:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:03:11 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 15 Mar 2023 23:28:17 GMT
ENV EMQX_VERSION=4.4.16
# Wed, 15 Mar 2023 23:28:17 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 15 Mar 2023 23:28:21 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="901b76ea2bee68729b75280740ca31b1af5b358d331422d1653dc342ee830324"; fi;     if [ ${arch} = "arm64" ]; then sha256="1224f53d0ee98390c286f3bbd9af2f294c2fa4ccb79342343d803fa234165c6e"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 15 Mar 2023 23:28:21 GMT
WORKDIR /opt/emqx
# Wed, 15 Mar 2023 23:28:22 GMT
USER emqx
# Wed, 15 Mar 2023 23:28:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 15 Mar 2023 23:28:22 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 15 Mar 2023 23:28:22 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 15 Mar 2023 23:28:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 15 Mar 2023 23:28:22 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396ee3d6a271f9fce1d0b1fd4fc0bd3a54cd9c9139a819de5351b130046fea9d`  
		Last Modified: Wed, 01 Mar 2023 05:04:03 GMT  
		Size: 2.6 MB (2569541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79aa88ad721c3aad2bd0e2aaccdbb555263a96f1e69f9f9e7e2e698cbd61acf`  
		Last Modified: Wed, 01 Mar 2023 05:04:02 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8943a0bcb1f0d0512ed4d4f6cb52cbb45f7497f16a74fda13d0ec343c375f626`  
		Last Modified: Wed, 15 Mar 2023 23:28:41 GMT  
		Size: 47.3 MB (47286141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a2b18c61a7d3a97a7493d4c03698ead2a79a6e9f45985619f41fd6df9fcc15`  
		Last Modified: Wed, 15 Mar 2023 23:28:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4.16` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4e9ebe772c56e5076b7d356635a535cf5565d54c26264c0848393a3a91f757a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72700283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e4a8802d3708ed0e9e04e9eba2393ce51bc8cae915d012bf4f4374b1d66882`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:21:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 03:21:03 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 15 Mar 2023 23:40:08 GMT
ENV EMQX_VERSION=4.4.16
# Wed, 15 Mar 2023 23:40:08 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 15 Mar 2023 23:40:11 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="901b76ea2bee68729b75280740ca31b1af5b358d331422d1653dc342ee830324"; fi;     if [ ${arch} = "arm64" ]; then sha256="1224f53d0ee98390c286f3bbd9af2f294c2fa4ccb79342343d803fa234165c6e"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 15 Mar 2023 23:40:12 GMT
WORKDIR /opt/emqx
# Wed, 15 Mar 2023 23:40:12 GMT
USER emqx
# Wed, 15 Mar 2023 23:40:12 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 15 Mar 2023 23:40:12 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 15 Mar 2023 23:40:12 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 15 Mar 2023 23:40:12 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 15 Mar 2023 23:40:12 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ea117f9b26bad2c79fea1dafb19b2ccbfb0e0744061d7743a5aea0c0e38af7`  
		Last Modified: Wed, 01 Mar 2023 03:21:50 GMT  
		Size: 2.6 MB (2559230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fde159950f1c178189d5f614a5405bd1df5caabc1ebd2bfc1e35376f9bd0e19`  
		Last Modified: Wed, 01 Mar 2023 03:21:50 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4e303f3e8ae9c4c0212bb811a988e668b8fb253f34804cf455d4b4179c1ccf`  
		Last Modified: Wed, 15 Mar 2023 23:40:31 GMT  
		Size: 40.1 MB (40073017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209dd83a5db4a0f1352247f1e19e02a3a54ee87fb2e45771e96d01045483e4aa`  
		Last Modified: Wed, 15 Mar 2023 23:40:26 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5`

```console
$ docker pull emqx@sha256:46717cea11e956cb8edeb6b900efb34ead650e8ea5e34128b2f266a1dccb5a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:419cacf6195600e119273142f75802a43aa3345067a905da93afa3c6ef6352ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101213576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3da61ba7da85ea7d8a71e7377117d6f7e23f7c7a05787bf28600e87334a614`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:03:25 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:03:26 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Fri, 10 Mar 2023 20:19:39 GMT
ENV EMQX_VERSION=5.0.20
# Fri, 10 Mar 2023 20:19:39 GMT
ENV AMD64_SHA256=88711b32e20676d11e3101bbb0e655d9ebf045a7735c190df0c26a230db8fac0
# Fri, 10 Mar 2023 20:19:39 GMT
ENV ARM64_SHA256=519fb1b14478e7fcc9ca74017bb4b09355e5d90def0c5d807e11165864388cd9
# Fri, 10 Mar 2023 20:19:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 10 Mar 2023 20:19:44 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Fri, 10 Mar 2023 20:19:45 GMT
WORKDIR /opt/emqx
# Fri, 10 Mar 2023 20:19:45 GMT
USER emqx
# Fri, 10 Mar 2023 20:19:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 10 Mar 2023 20:19:45 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 10 Mar 2023 20:19:45 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 10 Mar 2023 20:19:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 10 Mar 2023 20:19:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a35a595ef04513102e76624112833df5aee4f5e7a95b61fa5eddc304211ab3`  
		Last Modified: Wed, 01 Mar 2023 05:04:19 GMT  
		Size: 3.0 MB (2987679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e798ac719c7147c6c2faada408a48221abe27042dbc139527a475289fd20c98a`  
		Last Modified: Wed, 01 Mar 2023 05:04:19 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eafb9c8208d3bccc697ced82005883b641d02d97977cba3529a803fe07f6df9`  
		Last Modified: Fri, 10 Mar 2023 20:20:26 GMT  
		Size: 66.8 MB (66809481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ede4f97a9c6b64ff913490d403d30cc16ce0befeb510b05b022918bae24e753`  
		Last Modified: Fri, 10 Mar 2023 20:20:18 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:13e95e2fef6dbd597b66a357807ceb71cba9ee2526562f9e3a1c1b8ccd84c33b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92303842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e912e5f1bdce506ce56157f5a78282b230d9c95b6700df96645f9f25e4dce4b5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:21:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 03:21:17 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Fri, 10 Mar 2023 21:48:23 GMT
ENV EMQX_VERSION=5.0.20
# Fri, 10 Mar 2023 21:48:23 GMT
ENV AMD64_SHA256=88711b32e20676d11e3101bbb0e655d9ebf045a7735c190df0c26a230db8fac0
# Fri, 10 Mar 2023 21:48:23 GMT
ENV ARM64_SHA256=519fb1b14478e7fcc9ca74017bb4b09355e5d90def0c5d807e11165864388cd9
# Fri, 10 Mar 2023 21:48:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 10 Mar 2023 21:48:27 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Fri, 10 Mar 2023 21:48:28 GMT
WORKDIR /opt/emqx
# Fri, 10 Mar 2023 21:48:28 GMT
USER emqx
# Fri, 10 Mar 2023 21:48:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 10 Mar 2023 21:48:28 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 10 Mar 2023 21:48:28 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 10 Mar 2023 21:48:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 10 Mar 2023 21:48:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38086ab7a191a5da95fb6158c384014d022c21f7e3615ad8b0cdd460c25f9035`  
		Last Modified: Wed, 01 Mar 2023 03:22:04 GMT  
		Size: 3.0 MB (3002759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54eeac58f385f878614093545595a71c10cb909203557c85c1b5ef5defba64d`  
		Last Modified: Wed, 01 Mar 2023 03:22:04 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b403af0a79322aefc651ac609b98935d96017c8baa135e28307c6e9cc0691aff`  
		Last Modified: Fri, 10 Mar 2023 21:49:03 GMT  
		Size: 59.2 MB (59233251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f7b75ab2328825c25f602efb49a16223ab44d99a65a2e8a15856390f623199`  
		Last Modified: Fri, 10 Mar 2023 21:48:57 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0`

```console
$ docker pull emqx@sha256:46717cea11e956cb8edeb6b900efb34ead650e8ea5e34128b2f266a1dccb5a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0` - linux; amd64

```console
$ docker pull emqx@sha256:419cacf6195600e119273142f75802a43aa3345067a905da93afa3c6ef6352ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101213576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3da61ba7da85ea7d8a71e7377117d6f7e23f7c7a05787bf28600e87334a614`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:03:25 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:03:26 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Fri, 10 Mar 2023 20:19:39 GMT
ENV EMQX_VERSION=5.0.20
# Fri, 10 Mar 2023 20:19:39 GMT
ENV AMD64_SHA256=88711b32e20676d11e3101bbb0e655d9ebf045a7735c190df0c26a230db8fac0
# Fri, 10 Mar 2023 20:19:39 GMT
ENV ARM64_SHA256=519fb1b14478e7fcc9ca74017bb4b09355e5d90def0c5d807e11165864388cd9
# Fri, 10 Mar 2023 20:19:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 10 Mar 2023 20:19:44 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Fri, 10 Mar 2023 20:19:45 GMT
WORKDIR /opt/emqx
# Fri, 10 Mar 2023 20:19:45 GMT
USER emqx
# Fri, 10 Mar 2023 20:19:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 10 Mar 2023 20:19:45 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 10 Mar 2023 20:19:45 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 10 Mar 2023 20:19:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 10 Mar 2023 20:19:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a35a595ef04513102e76624112833df5aee4f5e7a95b61fa5eddc304211ab3`  
		Last Modified: Wed, 01 Mar 2023 05:04:19 GMT  
		Size: 3.0 MB (2987679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e798ac719c7147c6c2faada408a48221abe27042dbc139527a475289fd20c98a`  
		Last Modified: Wed, 01 Mar 2023 05:04:19 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eafb9c8208d3bccc697ced82005883b641d02d97977cba3529a803fe07f6df9`  
		Last Modified: Fri, 10 Mar 2023 20:20:26 GMT  
		Size: 66.8 MB (66809481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ede4f97a9c6b64ff913490d403d30cc16ce0befeb510b05b022918bae24e753`  
		Last Modified: Fri, 10 Mar 2023 20:20:18 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:13e95e2fef6dbd597b66a357807ceb71cba9ee2526562f9e3a1c1b8ccd84c33b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92303842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e912e5f1bdce506ce56157f5a78282b230d9c95b6700df96645f9f25e4dce4b5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:21:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 03:21:17 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Fri, 10 Mar 2023 21:48:23 GMT
ENV EMQX_VERSION=5.0.20
# Fri, 10 Mar 2023 21:48:23 GMT
ENV AMD64_SHA256=88711b32e20676d11e3101bbb0e655d9ebf045a7735c190df0c26a230db8fac0
# Fri, 10 Mar 2023 21:48:23 GMT
ENV ARM64_SHA256=519fb1b14478e7fcc9ca74017bb4b09355e5d90def0c5d807e11165864388cd9
# Fri, 10 Mar 2023 21:48:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 10 Mar 2023 21:48:27 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Fri, 10 Mar 2023 21:48:28 GMT
WORKDIR /opt/emqx
# Fri, 10 Mar 2023 21:48:28 GMT
USER emqx
# Fri, 10 Mar 2023 21:48:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 10 Mar 2023 21:48:28 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 10 Mar 2023 21:48:28 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 10 Mar 2023 21:48:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 10 Mar 2023 21:48:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38086ab7a191a5da95fb6158c384014d022c21f7e3615ad8b0cdd460c25f9035`  
		Last Modified: Wed, 01 Mar 2023 03:22:04 GMT  
		Size: 3.0 MB (3002759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54eeac58f385f878614093545595a71c10cb909203557c85c1b5ef5defba64d`  
		Last Modified: Wed, 01 Mar 2023 03:22:04 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b403af0a79322aefc651ac609b98935d96017c8baa135e28307c6e9cc0691aff`  
		Last Modified: Fri, 10 Mar 2023 21:49:03 GMT  
		Size: 59.2 MB (59233251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f7b75ab2328825c25f602efb49a16223ab44d99a65a2e8a15856390f623199`  
		Last Modified: Fri, 10 Mar 2023 21:48:57 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0.20`

```console
$ docker pull emqx@sha256:46717cea11e956cb8edeb6b900efb34ead650e8ea5e34128b2f266a1dccb5a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0.20` - linux; amd64

```console
$ docker pull emqx@sha256:419cacf6195600e119273142f75802a43aa3345067a905da93afa3c6ef6352ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101213576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3da61ba7da85ea7d8a71e7377117d6f7e23f7c7a05787bf28600e87334a614`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:03:25 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:03:26 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Fri, 10 Mar 2023 20:19:39 GMT
ENV EMQX_VERSION=5.0.20
# Fri, 10 Mar 2023 20:19:39 GMT
ENV AMD64_SHA256=88711b32e20676d11e3101bbb0e655d9ebf045a7735c190df0c26a230db8fac0
# Fri, 10 Mar 2023 20:19:39 GMT
ENV ARM64_SHA256=519fb1b14478e7fcc9ca74017bb4b09355e5d90def0c5d807e11165864388cd9
# Fri, 10 Mar 2023 20:19:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 10 Mar 2023 20:19:44 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Fri, 10 Mar 2023 20:19:45 GMT
WORKDIR /opt/emqx
# Fri, 10 Mar 2023 20:19:45 GMT
USER emqx
# Fri, 10 Mar 2023 20:19:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 10 Mar 2023 20:19:45 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 10 Mar 2023 20:19:45 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 10 Mar 2023 20:19:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 10 Mar 2023 20:19:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a35a595ef04513102e76624112833df5aee4f5e7a95b61fa5eddc304211ab3`  
		Last Modified: Wed, 01 Mar 2023 05:04:19 GMT  
		Size: 3.0 MB (2987679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e798ac719c7147c6c2faada408a48221abe27042dbc139527a475289fd20c98a`  
		Last Modified: Wed, 01 Mar 2023 05:04:19 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eafb9c8208d3bccc697ced82005883b641d02d97977cba3529a803fe07f6df9`  
		Last Modified: Fri, 10 Mar 2023 20:20:26 GMT  
		Size: 66.8 MB (66809481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ede4f97a9c6b64ff913490d403d30cc16ce0befeb510b05b022918bae24e753`  
		Last Modified: Fri, 10 Mar 2023 20:20:18 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0.20` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:13e95e2fef6dbd597b66a357807ceb71cba9ee2526562f9e3a1c1b8ccd84c33b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92303842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e912e5f1bdce506ce56157f5a78282b230d9c95b6700df96645f9f25e4dce4b5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:21:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 03:21:17 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Fri, 10 Mar 2023 21:48:23 GMT
ENV EMQX_VERSION=5.0.20
# Fri, 10 Mar 2023 21:48:23 GMT
ENV AMD64_SHA256=88711b32e20676d11e3101bbb0e655d9ebf045a7735c190df0c26a230db8fac0
# Fri, 10 Mar 2023 21:48:23 GMT
ENV ARM64_SHA256=519fb1b14478e7fcc9ca74017bb4b09355e5d90def0c5d807e11165864388cd9
# Fri, 10 Mar 2023 21:48:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 10 Mar 2023 21:48:27 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Fri, 10 Mar 2023 21:48:28 GMT
WORKDIR /opt/emqx
# Fri, 10 Mar 2023 21:48:28 GMT
USER emqx
# Fri, 10 Mar 2023 21:48:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 10 Mar 2023 21:48:28 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 10 Mar 2023 21:48:28 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 10 Mar 2023 21:48:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 10 Mar 2023 21:48:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38086ab7a191a5da95fb6158c384014d022c21f7e3615ad8b0cdd460c25f9035`  
		Last Modified: Wed, 01 Mar 2023 03:22:04 GMT  
		Size: 3.0 MB (3002759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54eeac58f385f878614093545595a71c10cb909203557c85c1b5ef5defba64d`  
		Last Modified: Wed, 01 Mar 2023 03:22:04 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b403af0a79322aefc651ac609b98935d96017c8baa135e28307c6e9cc0691aff`  
		Last Modified: Fri, 10 Mar 2023 21:49:03 GMT  
		Size: 59.2 MB (59233251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f7b75ab2328825c25f602efb49a16223ab44d99a65a2e8a15856390f623199`  
		Last Modified: Fri, 10 Mar 2023 21:48:57 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:46717cea11e956cb8edeb6b900efb34ead650e8ea5e34128b2f266a1dccb5a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:419cacf6195600e119273142f75802a43aa3345067a905da93afa3c6ef6352ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101213576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3da61ba7da85ea7d8a71e7377117d6f7e23f7c7a05787bf28600e87334a614`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:03:25 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:03:26 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Fri, 10 Mar 2023 20:19:39 GMT
ENV EMQX_VERSION=5.0.20
# Fri, 10 Mar 2023 20:19:39 GMT
ENV AMD64_SHA256=88711b32e20676d11e3101bbb0e655d9ebf045a7735c190df0c26a230db8fac0
# Fri, 10 Mar 2023 20:19:39 GMT
ENV ARM64_SHA256=519fb1b14478e7fcc9ca74017bb4b09355e5d90def0c5d807e11165864388cd9
# Fri, 10 Mar 2023 20:19:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 10 Mar 2023 20:19:44 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Fri, 10 Mar 2023 20:19:45 GMT
WORKDIR /opt/emqx
# Fri, 10 Mar 2023 20:19:45 GMT
USER emqx
# Fri, 10 Mar 2023 20:19:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 10 Mar 2023 20:19:45 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 10 Mar 2023 20:19:45 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 10 Mar 2023 20:19:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 10 Mar 2023 20:19:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a35a595ef04513102e76624112833df5aee4f5e7a95b61fa5eddc304211ab3`  
		Last Modified: Wed, 01 Mar 2023 05:04:19 GMT  
		Size: 3.0 MB (2987679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e798ac719c7147c6c2faada408a48221abe27042dbc139527a475289fd20c98a`  
		Last Modified: Wed, 01 Mar 2023 05:04:19 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eafb9c8208d3bccc697ced82005883b641d02d97977cba3529a803fe07f6df9`  
		Last Modified: Fri, 10 Mar 2023 20:20:26 GMT  
		Size: 66.8 MB (66809481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ede4f97a9c6b64ff913490d403d30cc16ce0befeb510b05b022918bae24e753`  
		Last Modified: Fri, 10 Mar 2023 20:20:18 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:13e95e2fef6dbd597b66a357807ceb71cba9ee2526562f9e3a1c1b8ccd84c33b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92303842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e912e5f1bdce506ce56157f5a78282b230d9c95b6700df96645f9f25e4dce4b5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:21:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 03:21:17 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Fri, 10 Mar 2023 21:48:23 GMT
ENV EMQX_VERSION=5.0.20
# Fri, 10 Mar 2023 21:48:23 GMT
ENV AMD64_SHA256=88711b32e20676d11e3101bbb0e655d9ebf045a7735c190df0c26a230db8fac0
# Fri, 10 Mar 2023 21:48:23 GMT
ENV ARM64_SHA256=519fb1b14478e7fcc9ca74017bb4b09355e5d90def0c5d807e11165864388cd9
# Fri, 10 Mar 2023 21:48:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 10 Mar 2023 21:48:27 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Fri, 10 Mar 2023 21:48:28 GMT
WORKDIR /opt/emqx
# Fri, 10 Mar 2023 21:48:28 GMT
USER emqx
# Fri, 10 Mar 2023 21:48:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 10 Mar 2023 21:48:28 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Fri, 10 Mar 2023 21:48:28 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Fri, 10 Mar 2023 21:48:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 10 Mar 2023 21:48:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38086ab7a191a5da95fb6158c384014d022c21f7e3615ad8b0cdd460c25f9035`  
		Last Modified: Wed, 01 Mar 2023 03:22:04 GMT  
		Size: 3.0 MB (3002759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54eeac58f385f878614093545595a71c10cb909203557c85c1b5ef5defba64d`  
		Last Modified: Wed, 01 Mar 2023 03:22:04 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b403af0a79322aefc651ac609b98935d96017c8baa135e28307c6e9cc0691aff`  
		Last Modified: Fri, 10 Mar 2023 21:49:03 GMT  
		Size: 59.2 MB (59233251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f7b75ab2328825c25f602efb49a16223ab44d99a65a2e8a15856390f623199`  
		Last Modified: Fri, 10 Mar 2023 21:48:57 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
