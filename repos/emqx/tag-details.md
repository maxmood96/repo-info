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
$ docker pull emqx@sha256:0e9343dbb3dbcca6a02690d575ab57f5f11dcd2efde45b3e1acc3bebe536b06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:6a14406b3709ca58cddc419ab1be3d038ec906678f59c1c8dfe0bf8a5b5d8a82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124853978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0517be0738f3f49939248c10fda1fabcccc595724959bb499b23fc6715c860f4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:59:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:59:24 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 25 Oct 2022 02:59:25 GMT
ENV OTP=otp24.1.5-3
# Tue, 25 Oct 2022 02:59:29 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 25 Oct 2022 02:59:35 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 25 Oct 2022 02:59:35 GMT
WORKDIR /opt/emqx
# Tue, 25 Oct 2022 02:59:36 GMT
USER emqx
# Tue, 25 Oct 2022 02:59:36 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Oct 2022 02:59:36 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 25 Oct 2022 02:59:36 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 25 Oct 2022 02:59:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 02:59:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d74aaf56efa5133b3013772f289a177e4ca77677fa3a9c47129df9accb5c5b`  
		Last Modified: Tue, 25 Oct 2022 03:00:04 GMT  
		Size: 2.6 MB (2570980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e31e444f54589c1eb9f22aeeb8be2a989c01b19cae5b441e2e3fff82afb395`  
		Last Modified: Tue, 25 Oct 2022 03:00:08 GMT  
		Size: 45.4 MB (45424512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed69e4861c423a1a2dd9d103a29c0b06cd85611aec57ed628beb7ebf2a7a3dae`  
		Last Modified: Tue, 25 Oct 2022 03:00:08 GMT  
		Size: 45.4 MB (45437341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d71dc161d50458f0bb157d8141a0de75894e359e2d0ce9d5b2ecdb7cc0c85e0`  
		Last Modified: Tue, 25 Oct 2022 03:00:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b96eb9baf9f59f5524f82adfbe01e9ef5c01e081bb4b7b61847de59a7ad562fb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110236571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6eebb68d3555822f6610bc02400972790c4e0f2bae2ba0b827e1618e38ac76`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:13:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 06:13:29 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 15 Nov 2022 06:13:29 GMT
ENV OTP=otp24.1.5-3
# Tue, 15 Nov 2022 06:13:32 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 15 Nov 2022 06:13:36 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 15 Nov 2022 06:13:37 GMT
WORKDIR /opt/emqx
# Tue, 15 Nov 2022 06:13:37 GMT
USER emqx
# Tue, 15 Nov 2022 06:13:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 15 Nov 2022 06:13:37 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 15 Nov 2022 06:13:37 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 15 Nov 2022 06:13:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 15 Nov 2022 06:13:37 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad108ef5d5673e32622aa158fbc152df7e8c340c7f4e79efffecd4c5d6c2a7be`  
		Last Modified: Tue, 15 Nov 2022 06:14:09 GMT  
		Size: 2.6 MB (2560816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96042e2ccd2609d9b280266d2cc3063aab600802b597ec18244c2761f3af513`  
		Last Modified: Tue, 15 Nov 2022 06:14:11 GMT  
		Size: 38.8 MB (38806727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432b8a52dff2f8fc12cecf2988e77261a173d791f10a1ccedb107ace30b8fdf0`  
		Last Modified: Tue, 15 Nov 2022 06:14:11 GMT  
		Size: 38.8 MB (38807317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4504a627c078e5f88f9616bd61b3f0074e95a846d4bee00e1e4f6024bb61244`  
		Last Modified: Tue, 15 Nov 2022 06:14:08 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3`

```console
$ docker pull emqx@sha256:5d7c76ff33781921db98d45600a8c78b964425de8034fa057f9496f260dcafb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.3` - linux; amd64

```console
$ docker pull emqx@sha256:43536a67d4429cc8aa867fdf41039dd7e396f9f56490715fe3f32b0f806aa4dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103867129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7241d89833d419874337271105f686b7f2e2c5d430a0900ee3cb8c7e2dee6256`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:12 GMT
ADD file:14c4aa7a136ce9eb1fae0ba0f394509990d44126be801a2713cf8722fbb2e6b9 in / 
# Tue, 25 Oct 2022 01:44:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:59:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:59:03 GMT
ENV EMQX_VERSION=4.3.15
# Tue, 25 Oct 2022 02:59:07 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 25 Oct 2022 02:59:13 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 25 Oct 2022 02:59:13 GMT
WORKDIR /opt/emqx
# Tue, 25 Oct 2022 02:59:13 GMT
USER emqx
# Tue, 25 Oct 2022 02:59:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Oct 2022 02:59:13 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 25 Oct 2022 02:59:13 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 25 Oct 2022 02:59:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 02:59:14 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:4500a762c54620411ae491a547c66b61d577c1369ecbf5a7e91b4e153181854b`  
		Last Modified: Tue, 25 Oct 2022 01:48:40 GMT  
		Size: 27.1 MB (27140832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d619d62981391eba9cb8cf0c1de3e78ac9ec4eedd35f96f0842ae7598cc0880e`  
		Last Modified: Tue, 25 Oct 2022 02:59:49 GMT  
		Size: 4.6 MB (4612444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4f47eed4e4a2bece4b248f586388f8687f4f52184f3c70d0f20a284792e1bc`  
		Last Modified: Tue, 25 Oct 2022 02:59:52 GMT  
		Size: 36.1 MB (36056918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f8f173e104425373e2486c3f79eeca40ed850bae442d1e77c97d6551af0932`  
		Last Modified: Tue, 25 Oct 2022 02:59:53 GMT  
		Size: 36.1 MB (36055894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656e85600df981c2fbcc419979c0d583783a62cb8fd4f90aa11c64a60101aed0`  
		Last Modified: Tue, 25 Oct 2022 02:59:48 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:41d0b865a8ae856f8b872d7debd6cea5c3b88b5305741b6123aea500a084b2e4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101941144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db10c6572b2573057a3c57cd2a00999bd57ea1cfedb02e4f4c5bb7435b3d304`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:34 GMT
ADD file:aaead8e4dd08d41c8d1692bbe76b673119289836428e1f713ca550c2468711ac in / 
# Tue, 15 Nov 2022 01:41:34 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:13:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 06:13:13 GMT
ENV EMQX_VERSION=4.3.15
# Tue, 15 Nov 2022 06:13:16 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 15 Nov 2022 06:13:20 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 15 Nov 2022 06:13:21 GMT
WORKDIR /opt/emqx
# Tue, 15 Nov 2022 06:13:21 GMT
USER emqx
# Tue, 15 Nov 2022 06:13:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 15 Nov 2022 06:13:21 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 15 Nov 2022 06:13:21 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 15 Nov 2022 06:13:21 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 15 Nov 2022 06:13:21 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:cc457132e077d684a6cecad3331c35341d814c5d364f3cf24d698a6d8e76d0e7`  
		Last Modified: Tue, 15 Nov 2022 01:45:13 GMT  
		Size: 25.9 MB (25914924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d027abecdd5af35e9a16c44518f0617af3a9b80b03d0fac7e90d16f1de3c6100`  
		Last Modified: Tue, 15 Nov 2022 06:13:52 GMT  
		Size: 4.5 MB (4490492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35bd45a31f146e3d3b0af0147d4d492d45872372c83ebdc32e15129498c485e`  
		Last Modified: Tue, 15 Nov 2022 06:13:58 GMT  
		Size: 35.8 MB (35761772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6749b66844622561c7c7de00810191fad38032463dbd3288e9a4fdbd1323e41`  
		Last Modified: Tue, 15 Nov 2022 06:13:55 GMT  
		Size: 35.8 MB (35772916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21ae72d82eb83adc78c809979e9c1b9290e137e25e0d5bb0adb275fe6db6681`  
		Last Modified: Tue, 15 Nov 2022 06:13:51 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3.15`

```console
$ docker pull emqx@sha256:5d7c76ff33781921db98d45600a8c78b964425de8034fa057f9496f260dcafb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.3.15` - linux; amd64

```console
$ docker pull emqx@sha256:43536a67d4429cc8aa867fdf41039dd7e396f9f56490715fe3f32b0f806aa4dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103867129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7241d89833d419874337271105f686b7f2e2c5d430a0900ee3cb8c7e2dee6256`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:12 GMT
ADD file:14c4aa7a136ce9eb1fae0ba0f394509990d44126be801a2713cf8722fbb2e6b9 in / 
# Tue, 25 Oct 2022 01:44:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:59:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:59:03 GMT
ENV EMQX_VERSION=4.3.15
# Tue, 25 Oct 2022 02:59:07 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 25 Oct 2022 02:59:13 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 25 Oct 2022 02:59:13 GMT
WORKDIR /opt/emqx
# Tue, 25 Oct 2022 02:59:13 GMT
USER emqx
# Tue, 25 Oct 2022 02:59:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Oct 2022 02:59:13 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 25 Oct 2022 02:59:13 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 25 Oct 2022 02:59:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 02:59:14 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:4500a762c54620411ae491a547c66b61d577c1369ecbf5a7e91b4e153181854b`  
		Last Modified: Tue, 25 Oct 2022 01:48:40 GMT  
		Size: 27.1 MB (27140832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d619d62981391eba9cb8cf0c1de3e78ac9ec4eedd35f96f0842ae7598cc0880e`  
		Last Modified: Tue, 25 Oct 2022 02:59:49 GMT  
		Size: 4.6 MB (4612444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4f47eed4e4a2bece4b248f586388f8687f4f52184f3c70d0f20a284792e1bc`  
		Last Modified: Tue, 25 Oct 2022 02:59:52 GMT  
		Size: 36.1 MB (36056918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f8f173e104425373e2486c3f79eeca40ed850bae442d1e77c97d6551af0932`  
		Last Modified: Tue, 25 Oct 2022 02:59:53 GMT  
		Size: 36.1 MB (36055894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656e85600df981c2fbcc419979c0d583783a62cb8fd4f90aa11c64a60101aed0`  
		Last Modified: Tue, 25 Oct 2022 02:59:48 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.3.15` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:41d0b865a8ae856f8b872d7debd6cea5c3b88b5305741b6123aea500a084b2e4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101941144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db10c6572b2573057a3c57cd2a00999bd57ea1cfedb02e4f4c5bb7435b3d304`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:34 GMT
ADD file:aaead8e4dd08d41c8d1692bbe76b673119289836428e1f713ca550c2468711ac in / 
# Tue, 15 Nov 2022 01:41:34 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:13:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 06:13:13 GMT
ENV EMQX_VERSION=4.3.15
# Tue, 15 Nov 2022 06:13:16 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 15 Nov 2022 06:13:20 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 15 Nov 2022 06:13:21 GMT
WORKDIR /opt/emqx
# Tue, 15 Nov 2022 06:13:21 GMT
USER emqx
# Tue, 15 Nov 2022 06:13:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 15 Nov 2022 06:13:21 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 15 Nov 2022 06:13:21 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 15 Nov 2022 06:13:21 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 15 Nov 2022 06:13:21 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:cc457132e077d684a6cecad3331c35341d814c5d364f3cf24d698a6d8e76d0e7`  
		Last Modified: Tue, 15 Nov 2022 01:45:13 GMT  
		Size: 25.9 MB (25914924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d027abecdd5af35e9a16c44518f0617af3a9b80b03d0fac7e90d16f1de3c6100`  
		Last Modified: Tue, 15 Nov 2022 06:13:52 GMT  
		Size: 4.5 MB (4490492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35bd45a31f146e3d3b0af0147d4d492d45872372c83ebdc32e15129498c485e`  
		Last Modified: Tue, 15 Nov 2022 06:13:58 GMT  
		Size: 35.8 MB (35761772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6749b66844622561c7c7de00810191fad38032463dbd3288e9a4fdbd1323e41`  
		Last Modified: Tue, 15 Nov 2022 06:13:55 GMT  
		Size: 35.8 MB (35772916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21ae72d82eb83adc78c809979e9c1b9290e137e25e0d5bb0adb275fe6db6681`  
		Last Modified: Tue, 15 Nov 2022 06:13:51 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:0e9343dbb3dbcca6a02690d575ab57f5f11dcd2efde45b3e1acc3bebe536b06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:6a14406b3709ca58cddc419ab1be3d038ec906678f59c1c8dfe0bf8a5b5d8a82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124853978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0517be0738f3f49939248c10fda1fabcccc595724959bb499b23fc6715c860f4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:59:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:59:24 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 25 Oct 2022 02:59:25 GMT
ENV OTP=otp24.1.5-3
# Tue, 25 Oct 2022 02:59:29 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 25 Oct 2022 02:59:35 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 25 Oct 2022 02:59:35 GMT
WORKDIR /opt/emqx
# Tue, 25 Oct 2022 02:59:36 GMT
USER emqx
# Tue, 25 Oct 2022 02:59:36 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Oct 2022 02:59:36 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 25 Oct 2022 02:59:36 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 25 Oct 2022 02:59:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 02:59:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d74aaf56efa5133b3013772f289a177e4ca77677fa3a9c47129df9accb5c5b`  
		Last Modified: Tue, 25 Oct 2022 03:00:04 GMT  
		Size: 2.6 MB (2570980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e31e444f54589c1eb9f22aeeb8be2a989c01b19cae5b441e2e3fff82afb395`  
		Last Modified: Tue, 25 Oct 2022 03:00:08 GMT  
		Size: 45.4 MB (45424512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed69e4861c423a1a2dd9d103a29c0b06cd85611aec57ed628beb7ebf2a7a3dae`  
		Last Modified: Tue, 25 Oct 2022 03:00:08 GMT  
		Size: 45.4 MB (45437341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d71dc161d50458f0bb157d8141a0de75894e359e2d0ce9d5b2ecdb7cc0c85e0`  
		Last Modified: Tue, 25 Oct 2022 03:00:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b96eb9baf9f59f5524f82adfbe01e9ef5c01e081bb4b7b61847de59a7ad562fb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110236571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6eebb68d3555822f6610bc02400972790c4e0f2bae2ba0b827e1618e38ac76`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:13:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 06:13:29 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 15 Nov 2022 06:13:29 GMT
ENV OTP=otp24.1.5-3
# Tue, 15 Nov 2022 06:13:32 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 15 Nov 2022 06:13:36 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 15 Nov 2022 06:13:37 GMT
WORKDIR /opt/emqx
# Tue, 15 Nov 2022 06:13:37 GMT
USER emqx
# Tue, 15 Nov 2022 06:13:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 15 Nov 2022 06:13:37 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 15 Nov 2022 06:13:37 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 15 Nov 2022 06:13:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 15 Nov 2022 06:13:37 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad108ef5d5673e32622aa158fbc152df7e8c340c7f4e79efffecd4c5d6c2a7be`  
		Last Modified: Tue, 15 Nov 2022 06:14:09 GMT  
		Size: 2.6 MB (2560816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96042e2ccd2609d9b280266d2cc3063aab600802b597ec18244c2761f3af513`  
		Last Modified: Tue, 15 Nov 2022 06:14:11 GMT  
		Size: 38.8 MB (38806727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432b8a52dff2f8fc12cecf2988e77261a173d791f10a1ccedb107ace30b8fdf0`  
		Last Modified: Tue, 15 Nov 2022 06:14:11 GMT  
		Size: 38.8 MB (38807317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4504a627c078e5f88f9616bd61b3f0074e95a846d4bee00e1e4f6024bb61244`  
		Last Modified: Tue, 15 Nov 2022 06:14:08 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.4`

```console
$ docker pull emqx@sha256:0e9343dbb3dbcca6a02690d575ab57f5f11dcd2efde45b3e1acc3bebe536b06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4.4` - linux; amd64

```console
$ docker pull emqx@sha256:6a14406b3709ca58cddc419ab1be3d038ec906678f59c1c8dfe0bf8a5b5d8a82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124853978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0517be0738f3f49939248c10fda1fabcccc595724959bb499b23fc6715c860f4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:59:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:59:24 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 25 Oct 2022 02:59:25 GMT
ENV OTP=otp24.1.5-3
# Tue, 25 Oct 2022 02:59:29 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 25 Oct 2022 02:59:35 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 25 Oct 2022 02:59:35 GMT
WORKDIR /opt/emqx
# Tue, 25 Oct 2022 02:59:36 GMT
USER emqx
# Tue, 25 Oct 2022 02:59:36 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Oct 2022 02:59:36 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 25 Oct 2022 02:59:36 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 25 Oct 2022 02:59:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 02:59:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d74aaf56efa5133b3013772f289a177e4ca77677fa3a9c47129df9accb5c5b`  
		Last Modified: Tue, 25 Oct 2022 03:00:04 GMT  
		Size: 2.6 MB (2570980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e31e444f54589c1eb9f22aeeb8be2a989c01b19cae5b441e2e3fff82afb395`  
		Last Modified: Tue, 25 Oct 2022 03:00:08 GMT  
		Size: 45.4 MB (45424512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed69e4861c423a1a2dd9d103a29c0b06cd85611aec57ed628beb7ebf2a7a3dae`  
		Last Modified: Tue, 25 Oct 2022 03:00:08 GMT  
		Size: 45.4 MB (45437341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d71dc161d50458f0bb157d8141a0de75894e359e2d0ce9d5b2ecdb7cc0c85e0`  
		Last Modified: Tue, 25 Oct 2022 03:00:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b96eb9baf9f59f5524f82adfbe01e9ef5c01e081bb4b7b61847de59a7ad562fb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110236571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6eebb68d3555822f6610bc02400972790c4e0f2bae2ba0b827e1618e38ac76`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:13:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 06:13:29 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 15 Nov 2022 06:13:29 GMT
ENV OTP=otp24.1.5-3
# Tue, 15 Nov 2022 06:13:32 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 15 Nov 2022 06:13:36 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 15 Nov 2022 06:13:37 GMT
WORKDIR /opt/emqx
# Tue, 15 Nov 2022 06:13:37 GMT
USER emqx
# Tue, 15 Nov 2022 06:13:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 15 Nov 2022 06:13:37 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 15 Nov 2022 06:13:37 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 15 Nov 2022 06:13:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 15 Nov 2022 06:13:37 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad108ef5d5673e32622aa158fbc152df7e8c340c7f4e79efffecd4c5d6c2a7be`  
		Last Modified: Tue, 15 Nov 2022 06:14:09 GMT  
		Size: 2.6 MB (2560816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96042e2ccd2609d9b280266d2cc3063aab600802b597ec18244c2761f3af513`  
		Last Modified: Tue, 15 Nov 2022 06:14:11 GMT  
		Size: 38.8 MB (38806727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432b8a52dff2f8fc12cecf2988e77261a173d791f10a1ccedb107ace30b8fdf0`  
		Last Modified: Tue, 15 Nov 2022 06:14:11 GMT  
		Size: 38.8 MB (38807317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4504a627c078e5f88f9616bd61b3f0074e95a846d4bee00e1e4f6024bb61244`  
		Last Modified: Tue, 15 Nov 2022 06:14:08 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:0e9343dbb3dbcca6a02690d575ab57f5f11dcd2efde45b3e1acc3bebe536b06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:6a14406b3709ca58cddc419ab1be3d038ec906678f59c1c8dfe0bf8a5b5d8a82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124853978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0517be0738f3f49939248c10fda1fabcccc595724959bb499b23fc6715c860f4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:59:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:59:24 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 25 Oct 2022 02:59:25 GMT
ENV OTP=otp24.1.5-3
# Tue, 25 Oct 2022 02:59:29 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 25 Oct 2022 02:59:35 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 25 Oct 2022 02:59:35 GMT
WORKDIR /opt/emqx
# Tue, 25 Oct 2022 02:59:36 GMT
USER emqx
# Tue, 25 Oct 2022 02:59:36 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Oct 2022 02:59:36 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 25 Oct 2022 02:59:36 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 25 Oct 2022 02:59:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 02:59:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d74aaf56efa5133b3013772f289a177e4ca77677fa3a9c47129df9accb5c5b`  
		Last Modified: Tue, 25 Oct 2022 03:00:04 GMT  
		Size: 2.6 MB (2570980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e31e444f54589c1eb9f22aeeb8be2a989c01b19cae5b441e2e3fff82afb395`  
		Last Modified: Tue, 25 Oct 2022 03:00:08 GMT  
		Size: 45.4 MB (45424512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed69e4861c423a1a2dd9d103a29c0b06cd85611aec57ed628beb7ebf2a7a3dae`  
		Last Modified: Tue, 25 Oct 2022 03:00:08 GMT  
		Size: 45.4 MB (45437341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d71dc161d50458f0bb157d8141a0de75894e359e2d0ce9d5b2ecdb7cc0c85e0`  
		Last Modified: Tue, 25 Oct 2022 03:00:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b96eb9baf9f59f5524f82adfbe01e9ef5c01e081bb4b7b61847de59a7ad562fb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110236571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6eebb68d3555822f6610bc02400972790c4e0f2bae2ba0b827e1618e38ac76`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:13:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 06:13:29 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 15 Nov 2022 06:13:29 GMT
ENV OTP=otp24.1.5-3
# Tue, 15 Nov 2022 06:13:32 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 15 Nov 2022 06:13:36 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 15 Nov 2022 06:13:37 GMT
WORKDIR /opt/emqx
# Tue, 15 Nov 2022 06:13:37 GMT
USER emqx
# Tue, 15 Nov 2022 06:13:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 15 Nov 2022 06:13:37 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 15 Nov 2022 06:13:37 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 15 Nov 2022 06:13:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 15 Nov 2022 06:13:37 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad108ef5d5673e32622aa158fbc152df7e8c340c7f4e79efffecd4c5d6c2a7be`  
		Last Modified: Tue, 15 Nov 2022 06:14:09 GMT  
		Size: 2.6 MB (2560816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96042e2ccd2609d9b280266d2cc3063aab600802b597ec18244c2761f3af513`  
		Last Modified: Tue, 15 Nov 2022 06:14:11 GMT  
		Size: 38.8 MB (38806727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432b8a52dff2f8fc12cecf2988e77261a173d791f10a1ccedb107ace30b8fdf0`  
		Last Modified: Tue, 15 Nov 2022 06:14:11 GMT  
		Size: 38.8 MB (38807317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4504a627c078e5f88f9616bd61b3f0074e95a846d4bee00e1e4f6024bb61244`  
		Last Modified: Tue, 15 Nov 2022 06:14:08 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
