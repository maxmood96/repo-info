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
$ docker pull emqx@sha256:8913fd30fd92a190bc5a13504a7506db08555abfba1ede5877ffe7f9e5ba20c5
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
$ docker pull emqx@sha256:cb49dd1643174b37c635368260d07662a8511e96689793ae8d7e04ff18e1accf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110239886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9258b65d71f38328159501cad931745d138ad3f6a73f5171d396d0f36700afa2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:44:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:44:59 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 25 Oct 2022 08:44:59 GMT
ENV OTP=otp24.1.5-3
# Tue, 25 Oct 2022 08:45:02 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 25 Oct 2022 08:45:06 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 25 Oct 2022 08:45:07 GMT
WORKDIR /opt/emqx
# Tue, 25 Oct 2022 08:45:07 GMT
USER emqx
# Tue, 25 Oct 2022 08:45:07 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Oct 2022 08:45:07 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 25 Oct 2022 08:45:07 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 25 Oct 2022 08:45:07 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:45:07 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1052f237e0c3d57582a1eb36913676b9fb50dc092e9fa4f3dfcb38916914a4cb`  
		Last Modified: Tue, 25 Oct 2022 08:45:34 GMT  
		Size: 2.6 MB (2560863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d473c577b40437811942357bccba6fab61c82cc19b48341de23016e1d56b8d`  
		Last Modified: Tue, 25 Oct 2022 08:45:38 GMT  
		Size: 38.8 MB (38806725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c200d97fc57536dbcd12fd40851179d95ea294f1748719df7c1a040bfac49cde`  
		Last Modified: Tue, 25 Oct 2022 08:45:38 GMT  
		Size: 38.8 MB (38807280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9222b05a2b36232eb4660a628c9ab316fde1da5e4b305ebc9da64fe057904d`  
		Last Modified: Tue, 25 Oct 2022 08:45:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3`

```console
$ docker pull emqx@sha256:e3018be2ef45e7fed2e7947d816c7e3d4237046875afc6973bc58a5610684641
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
$ docker pull emqx@sha256:e99182fd86acbdb616d5aad5bf0c3095044ec87cf03b96436b8a0383a8fe82c0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101940992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecf329e7cd2fc75761aacb0ffa972756036db0f375197019183f8b739b063e3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:13 GMT
ADD file:342233874a06722375663380e7e3a04502a995dfbbc425cd1913f10e96a50dcb in / 
# Tue, 25 Oct 2022 05:46:14 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:44:44 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:44:44 GMT
ENV EMQX_VERSION=4.3.15
# Tue, 25 Oct 2022 08:44:47 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 25 Oct 2022 08:44:51 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 25 Oct 2022 08:44:51 GMT
WORKDIR /opt/emqx
# Tue, 25 Oct 2022 08:44:51 GMT
USER emqx
# Tue, 25 Oct 2022 08:44:52 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Oct 2022 08:44:52 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 25 Oct 2022 08:44:52 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 25 Oct 2022 08:44:52 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:44:52 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:5f30c56efde95016859c51bdc10e665dd57dc3c8d22e7abbf384ae9722dfa19e`  
		Last Modified: Tue, 25 Oct 2022 05:49:47 GMT  
		Size: 25.9 MB (25914885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcfe372e1dfc7137508ca7f45038fb00fdd800fb02b264a4a79206df1ac9bb9`  
		Last Modified: Tue, 25 Oct 2022 08:45:22 GMT  
		Size: 4.5 MB (4490384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b96bffc21cfacf284420c38e13a37bac329f882624acd0185211abc826e4b7`  
		Last Modified: Tue, 25 Oct 2022 08:45:24 GMT  
		Size: 35.8 MB (35761769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c5cbfae46581d7eb80d82c7023671c3e9e60e6f4e4d0e6950f5030c56f40`  
		Last Modified: Tue, 25 Oct 2022 08:45:25 GMT  
		Size: 35.8 MB (35772912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83c67359285fc06f243a3273e00d6ea49bda4cd4becf26b2935352380b13edd`  
		Last Modified: Tue, 25 Oct 2022 08:45:21 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3.15`

```console
$ docker pull emqx@sha256:e3018be2ef45e7fed2e7947d816c7e3d4237046875afc6973bc58a5610684641
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
$ docker pull emqx@sha256:e99182fd86acbdb616d5aad5bf0c3095044ec87cf03b96436b8a0383a8fe82c0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101940992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecf329e7cd2fc75761aacb0ffa972756036db0f375197019183f8b739b063e3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:13 GMT
ADD file:342233874a06722375663380e7e3a04502a995dfbbc425cd1913f10e96a50dcb in / 
# Tue, 25 Oct 2022 05:46:14 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:44:44 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:44:44 GMT
ENV EMQX_VERSION=4.3.15
# Tue, 25 Oct 2022 08:44:47 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 25 Oct 2022 08:44:51 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 25 Oct 2022 08:44:51 GMT
WORKDIR /opt/emqx
# Tue, 25 Oct 2022 08:44:51 GMT
USER emqx
# Tue, 25 Oct 2022 08:44:52 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Oct 2022 08:44:52 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 25 Oct 2022 08:44:52 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 25 Oct 2022 08:44:52 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:44:52 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:5f30c56efde95016859c51bdc10e665dd57dc3c8d22e7abbf384ae9722dfa19e`  
		Last Modified: Tue, 25 Oct 2022 05:49:47 GMT  
		Size: 25.9 MB (25914885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcfe372e1dfc7137508ca7f45038fb00fdd800fb02b264a4a79206df1ac9bb9`  
		Last Modified: Tue, 25 Oct 2022 08:45:22 GMT  
		Size: 4.5 MB (4490384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b96bffc21cfacf284420c38e13a37bac329f882624acd0185211abc826e4b7`  
		Last Modified: Tue, 25 Oct 2022 08:45:24 GMT  
		Size: 35.8 MB (35761769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad0c5cbfae46581d7eb80d82c7023671c3e9e60e6f4e4d0e6950f5030c56f40`  
		Last Modified: Tue, 25 Oct 2022 08:45:25 GMT  
		Size: 35.8 MB (35772912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83c67359285fc06f243a3273e00d6ea49bda4cd4becf26b2935352380b13edd`  
		Last Modified: Tue, 25 Oct 2022 08:45:21 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:8913fd30fd92a190bc5a13504a7506db08555abfba1ede5877ffe7f9e5ba20c5
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
$ docker pull emqx@sha256:cb49dd1643174b37c635368260d07662a8511e96689793ae8d7e04ff18e1accf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110239886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9258b65d71f38328159501cad931745d138ad3f6a73f5171d396d0f36700afa2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:44:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:44:59 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 25 Oct 2022 08:44:59 GMT
ENV OTP=otp24.1.5-3
# Tue, 25 Oct 2022 08:45:02 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 25 Oct 2022 08:45:06 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 25 Oct 2022 08:45:07 GMT
WORKDIR /opt/emqx
# Tue, 25 Oct 2022 08:45:07 GMT
USER emqx
# Tue, 25 Oct 2022 08:45:07 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Oct 2022 08:45:07 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 25 Oct 2022 08:45:07 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 25 Oct 2022 08:45:07 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:45:07 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1052f237e0c3d57582a1eb36913676b9fb50dc092e9fa4f3dfcb38916914a4cb`  
		Last Modified: Tue, 25 Oct 2022 08:45:34 GMT  
		Size: 2.6 MB (2560863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d473c577b40437811942357bccba6fab61c82cc19b48341de23016e1d56b8d`  
		Last Modified: Tue, 25 Oct 2022 08:45:38 GMT  
		Size: 38.8 MB (38806725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c200d97fc57536dbcd12fd40851179d95ea294f1748719df7c1a040bfac49cde`  
		Last Modified: Tue, 25 Oct 2022 08:45:38 GMT  
		Size: 38.8 MB (38807280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9222b05a2b36232eb4660a628c9ab316fde1da5e4b305ebc9da64fe057904d`  
		Last Modified: Tue, 25 Oct 2022 08:45:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.4`

```console
$ docker pull emqx@sha256:8913fd30fd92a190bc5a13504a7506db08555abfba1ede5877ffe7f9e5ba20c5
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
$ docker pull emqx@sha256:cb49dd1643174b37c635368260d07662a8511e96689793ae8d7e04ff18e1accf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110239886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9258b65d71f38328159501cad931745d138ad3f6a73f5171d396d0f36700afa2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:44:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:44:59 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 25 Oct 2022 08:44:59 GMT
ENV OTP=otp24.1.5-3
# Tue, 25 Oct 2022 08:45:02 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 25 Oct 2022 08:45:06 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 25 Oct 2022 08:45:07 GMT
WORKDIR /opt/emqx
# Tue, 25 Oct 2022 08:45:07 GMT
USER emqx
# Tue, 25 Oct 2022 08:45:07 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Oct 2022 08:45:07 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 25 Oct 2022 08:45:07 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 25 Oct 2022 08:45:07 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:45:07 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1052f237e0c3d57582a1eb36913676b9fb50dc092e9fa4f3dfcb38916914a4cb`  
		Last Modified: Tue, 25 Oct 2022 08:45:34 GMT  
		Size: 2.6 MB (2560863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d473c577b40437811942357bccba6fab61c82cc19b48341de23016e1d56b8d`  
		Last Modified: Tue, 25 Oct 2022 08:45:38 GMT  
		Size: 38.8 MB (38806725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c200d97fc57536dbcd12fd40851179d95ea294f1748719df7c1a040bfac49cde`  
		Last Modified: Tue, 25 Oct 2022 08:45:38 GMT  
		Size: 38.8 MB (38807280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9222b05a2b36232eb4660a628c9ab316fde1da5e4b305ebc9da64fe057904d`  
		Last Modified: Tue, 25 Oct 2022 08:45:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:8913fd30fd92a190bc5a13504a7506db08555abfba1ede5877ffe7f9e5ba20c5
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
$ docker pull emqx@sha256:cb49dd1643174b37c635368260d07662a8511e96689793ae8d7e04ff18e1accf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110239886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9258b65d71f38328159501cad931745d138ad3f6a73f5171d396d0f36700afa2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:44:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:44:59 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 25 Oct 2022 08:44:59 GMT
ENV OTP=otp24.1.5-3
# Tue, 25 Oct 2022 08:45:02 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 25 Oct 2022 08:45:06 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 25 Oct 2022 08:45:07 GMT
WORKDIR /opt/emqx
# Tue, 25 Oct 2022 08:45:07 GMT
USER emqx
# Tue, 25 Oct 2022 08:45:07 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Oct 2022 08:45:07 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 25 Oct 2022 08:45:07 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 25 Oct 2022 08:45:07 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:45:07 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1052f237e0c3d57582a1eb36913676b9fb50dc092e9fa4f3dfcb38916914a4cb`  
		Last Modified: Tue, 25 Oct 2022 08:45:34 GMT  
		Size: 2.6 MB (2560863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d473c577b40437811942357bccba6fab61c82cc19b48341de23016e1d56b8d`  
		Last Modified: Tue, 25 Oct 2022 08:45:38 GMT  
		Size: 38.8 MB (38806725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c200d97fc57536dbcd12fd40851179d95ea294f1748719df7c1a040bfac49cde`  
		Last Modified: Tue, 25 Oct 2022 08:45:38 GMT  
		Size: 38.8 MB (38807280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9222b05a2b36232eb4660a628c9ab316fde1da5e4b305ebc9da64fe057904d`  
		Last Modified: Tue, 25 Oct 2022 08:45:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
