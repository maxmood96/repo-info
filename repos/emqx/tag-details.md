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
$ docker pull emqx@sha256:85c635044a8c2360bb7f1d25c120ede0690f8da81d5e08094a62cce9b09482a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:796567727ce2511af60d905be66d967ea6d9e28d10d5f44ddc3c7c7ec9e44277
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124810496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9757ce7d3aee1450248b308f95ee70309ff97dcf69e6eebf3e5ba34a11976e8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:12:33 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:07:04 GMT
ENV EMQX_VERSION=4.4.4
# Fri, 24 Jun 2022 03:07:04 GMT
ENV OTP=otp24.1.5-3
# Fri, 24 Jun 2022 03:07:09 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Fri, 24 Jun 2022 03:07:14 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Fri, 24 Jun 2022 03:07:15 GMT
WORKDIR /opt/emqx
# Fri, 24 Jun 2022 03:07:15 GMT
USER emqx
# Fri, 24 Jun 2022 03:07:15 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 24 Jun 2022 03:07:15 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Fri, 24 Jun 2022 03:07:15 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Fri, 24 Jun 2022 03:07:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:07:15 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed78c561493a213bbc8ebf8252500454b30fb63ca7c60ba824b0ae5b7357c96`  
		Last Modified: Fri, 24 Jun 2022 03:07:43 GMT  
		Size: 2.6 MB (2568138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b245dbd31649435875f4c3515c747854ca42655767d215043ec7496042802c84`  
		Last Modified: Fri, 24 Jun 2022 03:07:48 GMT  
		Size: 45.4 MB (45424521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9110d8e7ad575de625c76b984ea97e22d7667897b548de80e37e4cc4f88df8`  
		Last Modified: Fri, 24 Jun 2022 03:07:48 GMT  
		Size: 45.4 MB (45437321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ede9ec66e2d0462920dfd4c60bdcc412e082f96c855cb1dc9b3c1f9c1dbedd7`  
		Last Modified: Fri, 24 Jun 2022 03:07:43 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:887d01d0faac32364f7a82d3d4d4d224ab97e3ff6092b314772f1e768ddd8a6c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109968373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba4bb5600fd5c88b0588d2ae8e4c502374d5fe108bc2a73a9255e93405e24fb`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 May 2022 00:46:59 GMT
ADD file:158a0e401328bd7c0d49b9e8539186098967218f1b1a8c811f4398d29b74397f in / 
# Wed, 11 May 2022 00:47:00 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:48:02 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:48:03 GMT
ENV EMQX_VERSION=4.4.3
# Wed, 11 May 2022 01:48:04 GMT
ENV OTP=otp24.1.5-3
# Wed, 11 May 2022 01:48:09 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="7f7305566b977ef64afd31fed5fa71f7e79a5a934bf792422ac03e4f12768b02"; fi;     if [ ${arch} = "arm64" ]; then sha256="34d3315c329de1d0fbf7419db1bff5007313f45de39e8be0ca5f04bad19f45a5"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 May 2022 01:48:10 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 May 2022 01:48:11 GMT
WORKDIR /opt/emqx
# Wed, 11 May 2022 01:48:11 GMT
USER emqx
# Wed, 11 May 2022 01:48:12 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 May 2022 01:48:13 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 May 2022 01:48:15 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 May 2022 01:48:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 May 2022 01:48:16 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:dfdd5ffb257742b891ccad9400a77dad2a6260b2451e0f5e48a9ade1d17a87ec`  
		Last Modified: Wed, 11 May 2022 00:53:46 GMT  
		Size: 30.1 MB (30065693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41aff1a51b467f4353bb41440f62b9e619e628b9ae3dce9c015dba39d943604f`  
		Last Modified: Wed, 11 May 2022 01:48:35 GMT  
		Size: 2.4 MB (2351167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed44caa74811db97a6a7048b7d8ddb5a25e1edd000c0bdb89601c6de2974595`  
		Last Modified: Wed, 11 May 2022 01:48:39 GMT  
		Size: 38.8 MB (38773530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee8ec3642d256f9ca93285fc5fba425343ec272ce50c6c9dcb89ac4bf3a8925`  
		Last Modified: Wed, 11 May 2022 01:48:40 GMT  
		Size: 38.8 MB (38776875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e7077a80db19beb0214216aeaf4feac06e3b677d57a99c6853a0578717fe85`  
		Last Modified: Wed, 11 May 2022 01:48:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3`

```console
$ docker pull emqx@sha256:e9ca2a94f67ef7b7491c98fff555d29b1c6f257c4d38f7cc3502a338421fc413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `emqx:4.3` - linux; amd64

```console
$ docker pull emqx@sha256:5622c7f5b60ec871c19999d0def44d3ace2f56502a87cb5604adf6254dcad1f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103864194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0979ddbbce3b15d8867a1f1bd347403115e47c43dd6eecb28a33431bb1407709`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Fri, 24 Jun 2022 03:06:47 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:06:47 GMT
ENV EMQX_VERSION=4.3.15
# Fri, 24 Jun 2022 03:06:56 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Fri, 24 Jun 2022 03:07:01 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Fri, 24 Jun 2022 03:07:01 GMT
WORKDIR /opt/emqx
# Fri, 24 Jun 2022 03:07:02 GMT
USER emqx
# Fri, 24 Jun 2022 03:07:02 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 24 Jun 2022 03:07:02 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Fri, 24 Jun 2022 03:07:02 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Fri, 24 Jun 2022 03:07:02 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:07:02 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55473173b42e523e1aed7df999dbe39cf0cc26c087a6ee21bfafaf0086dafeb`  
		Last Modified: Fri, 24 Jun 2022 03:07:29 GMT  
		Size: 4.6 MB (4610273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6dc8185e19ac22b6578b9ea72c01e74e538044f9c4dcea500d816ad3585315`  
		Last Modified: Fri, 24 Jun 2022 03:07:32 GMT  
		Size: 36.1 MB (36056938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2ee8c199fb5055ff888cc23ac959ebb3f89fbd8e73b7df77b33e7c9f18d3df`  
		Last Modified: Fri, 24 Jun 2022 03:07:32 GMT  
		Size: 36.1 MB (36055899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6c546f33da107e5865fd43e656a6463cd3472a70c848745958069a76b6257d`  
		Last Modified: Fri, 24 Jun 2022 03:07:28 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3.15`

```console
$ docker pull emqx@sha256:e9ca2a94f67ef7b7491c98fff555d29b1c6f257c4d38f7cc3502a338421fc413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `emqx:4.3.15` - linux; amd64

```console
$ docker pull emqx@sha256:5622c7f5b60ec871c19999d0def44d3ace2f56502a87cb5604adf6254dcad1f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103864194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0979ddbbce3b15d8867a1f1bd347403115e47c43dd6eecb28a33431bb1407709`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Fri, 24 Jun 2022 03:06:47 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:06:47 GMT
ENV EMQX_VERSION=4.3.15
# Fri, 24 Jun 2022 03:06:56 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Fri, 24 Jun 2022 03:07:01 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Fri, 24 Jun 2022 03:07:01 GMT
WORKDIR /opt/emqx
# Fri, 24 Jun 2022 03:07:02 GMT
USER emqx
# Fri, 24 Jun 2022 03:07:02 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 24 Jun 2022 03:07:02 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Fri, 24 Jun 2022 03:07:02 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Fri, 24 Jun 2022 03:07:02 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:07:02 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55473173b42e523e1aed7df999dbe39cf0cc26c087a6ee21bfafaf0086dafeb`  
		Last Modified: Fri, 24 Jun 2022 03:07:29 GMT  
		Size: 4.6 MB (4610273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6dc8185e19ac22b6578b9ea72c01e74e538044f9c4dcea500d816ad3585315`  
		Last Modified: Fri, 24 Jun 2022 03:07:32 GMT  
		Size: 36.1 MB (36056938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2ee8c199fb5055ff888cc23ac959ebb3f89fbd8e73b7df77b33e7c9f18d3df`  
		Last Modified: Fri, 24 Jun 2022 03:07:32 GMT  
		Size: 36.1 MB (36055899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6c546f33da107e5865fd43e656a6463cd3472a70c848745958069a76b6257d`  
		Last Modified: Fri, 24 Jun 2022 03:07:28 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:85c635044a8c2360bb7f1d25c120ede0690f8da81d5e08094a62cce9b09482a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:796567727ce2511af60d905be66d967ea6d9e28d10d5f44ddc3c7c7ec9e44277
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124810496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9757ce7d3aee1450248b308f95ee70309ff97dcf69e6eebf3e5ba34a11976e8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:12:33 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:07:04 GMT
ENV EMQX_VERSION=4.4.4
# Fri, 24 Jun 2022 03:07:04 GMT
ENV OTP=otp24.1.5-3
# Fri, 24 Jun 2022 03:07:09 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Fri, 24 Jun 2022 03:07:14 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Fri, 24 Jun 2022 03:07:15 GMT
WORKDIR /opt/emqx
# Fri, 24 Jun 2022 03:07:15 GMT
USER emqx
# Fri, 24 Jun 2022 03:07:15 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 24 Jun 2022 03:07:15 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Fri, 24 Jun 2022 03:07:15 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Fri, 24 Jun 2022 03:07:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:07:15 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed78c561493a213bbc8ebf8252500454b30fb63ca7c60ba824b0ae5b7357c96`  
		Last Modified: Fri, 24 Jun 2022 03:07:43 GMT  
		Size: 2.6 MB (2568138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b245dbd31649435875f4c3515c747854ca42655767d215043ec7496042802c84`  
		Last Modified: Fri, 24 Jun 2022 03:07:48 GMT  
		Size: 45.4 MB (45424521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9110d8e7ad575de625c76b984ea97e22d7667897b548de80e37e4cc4f88df8`  
		Last Modified: Fri, 24 Jun 2022 03:07:48 GMT  
		Size: 45.4 MB (45437321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ede9ec66e2d0462920dfd4c60bdcc412e082f96c855cb1dc9b3c1f9c1dbedd7`  
		Last Modified: Fri, 24 Jun 2022 03:07:43 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:887d01d0faac32364f7a82d3d4d4d224ab97e3ff6092b314772f1e768ddd8a6c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109968373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba4bb5600fd5c88b0588d2ae8e4c502374d5fe108bc2a73a9255e93405e24fb`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 May 2022 00:46:59 GMT
ADD file:158a0e401328bd7c0d49b9e8539186098967218f1b1a8c811f4398d29b74397f in / 
# Wed, 11 May 2022 00:47:00 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:48:02 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:48:03 GMT
ENV EMQX_VERSION=4.4.3
# Wed, 11 May 2022 01:48:04 GMT
ENV OTP=otp24.1.5-3
# Wed, 11 May 2022 01:48:09 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="7f7305566b977ef64afd31fed5fa71f7e79a5a934bf792422ac03e4f12768b02"; fi;     if [ ${arch} = "arm64" ]; then sha256="34d3315c329de1d0fbf7419db1bff5007313f45de39e8be0ca5f04bad19f45a5"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 May 2022 01:48:10 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 May 2022 01:48:11 GMT
WORKDIR /opt/emqx
# Wed, 11 May 2022 01:48:11 GMT
USER emqx
# Wed, 11 May 2022 01:48:12 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 May 2022 01:48:13 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 May 2022 01:48:15 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 May 2022 01:48:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 May 2022 01:48:16 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:dfdd5ffb257742b891ccad9400a77dad2a6260b2451e0f5e48a9ade1d17a87ec`  
		Last Modified: Wed, 11 May 2022 00:53:46 GMT  
		Size: 30.1 MB (30065693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41aff1a51b467f4353bb41440f62b9e619e628b9ae3dce9c015dba39d943604f`  
		Last Modified: Wed, 11 May 2022 01:48:35 GMT  
		Size: 2.4 MB (2351167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed44caa74811db97a6a7048b7d8ddb5a25e1edd000c0bdb89601c6de2974595`  
		Last Modified: Wed, 11 May 2022 01:48:39 GMT  
		Size: 38.8 MB (38773530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee8ec3642d256f9ca93285fc5fba425343ec272ce50c6c9dcb89ac4bf3a8925`  
		Last Modified: Wed, 11 May 2022 01:48:40 GMT  
		Size: 38.8 MB (38776875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e7077a80db19beb0214216aeaf4feac06e3b677d57a99c6853a0578717fe85`  
		Last Modified: Wed, 11 May 2022 01:48:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.4`

```console
$ docker pull emqx@sha256:4b1986aa735deef21b111c508be964631ee47815823de4e4544aecf9102f9721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `emqx:4.4.4` - linux; amd64

```console
$ docker pull emqx@sha256:796567727ce2511af60d905be66d967ea6d9e28d10d5f44ddc3c7c7ec9e44277
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124810496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9757ce7d3aee1450248b308f95ee70309ff97dcf69e6eebf3e5ba34a11976e8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:12:33 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:07:04 GMT
ENV EMQX_VERSION=4.4.4
# Fri, 24 Jun 2022 03:07:04 GMT
ENV OTP=otp24.1.5-3
# Fri, 24 Jun 2022 03:07:09 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Fri, 24 Jun 2022 03:07:14 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Fri, 24 Jun 2022 03:07:15 GMT
WORKDIR /opt/emqx
# Fri, 24 Jun 2022 03:07:15 GMT
USER emqx
# Fri, 24 Jun 2022 03:07:15 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 24 Jun 2022 03:07:15 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Fri, 24 Jun 2022 03:07:15 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Fri, 24 Jun 2022 03:07:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:07:15 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed78c561493a213bbc8ebf8252500454b30fb63ca7c60ba824b0ae5b7357c96`  
		Last Modified: Fri, 24 Jun 2022 03:07:43 GMT  
		Size: 2.6 MB (2568138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b245dbd31649435875f4c3515c747854ca42655767d215043ec7496042802c84`  
		Last Modified: Fri, 24 Jun 2022 03:07:48 GMT  
		Size: 45.4 MB (45424521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9110d8e7ad575de625c76b984ea97e22d7667897b548de80e37e4cc4f88df8`  
		Last Modified: Fri, 24 Jun 2022 03:07:48 GMT  
		Size: 45.4 MB (45437321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ede9ec66e2d0462920dfd4c60bdcc412e082f96c855cb1dc9b3c1f9c1dbedd7`  
		Last Modified: Fri, 24 Jun 2022 03:07:43 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:85c635044a8c2360bb7f1d25c120ede0690f8da81d5e08094a62cce9b09482a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:796567727ce2511af60d905be66d967ea6d9e28d10d5f44ddc3c7c7ec9e44277
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124810496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9757ce7d3aee1450248b308f95ee70309ff97dcf69e6eebf3e5ba34a11976e8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:12:33 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:07:04 GMT
ENV EMQX_VERSION=4.4.4
# Fri, 24 Jun 2022 03:07:04 GMT
ENV OTP=otp24.1.5-3
# Fri, 24 Jun 2022 03:07:09 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Fri, 24 Jun 2022 03:07:14 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Fri, 24 Jun 2022 03:07:15 GMT
WORKDIR /opt/emqx
# Fri, 24 Jun 2022 03:07:15 GMT
USER emqx
# Fri, 24 Jun 2022 03:07:15 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 24 Jun 2022 03:07:15 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Fri, 24 Jun 2022 03:07:15 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Fri, 24 Jun 2022 03:07:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 24 Jun 2022 03:07:15 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed78c561493a213bbc8ebf8252500454b30fb63ca7c60ba824b0ae5b7357c96`  
		Last Modified: Fri, 24 Jun 2022 03:07:43 GMT  
		Size: 2.6 MB (2568138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b245dbd31649435875f4c3515c747854ca42655767d215043ec7496042802c84`  
		Last Modified: Fri, 24 Jun 2022 03:07:48 GMT  
		Size: 45.4 MB (45424521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9110d8e7ad575de625c76b984ea97e22d7667897b548de80e37e4cc4f88df8`  
		Last Modified: Fri, 24 Jun 2022 03:07:48 GMT  
		Size: 45.4 MB (45437321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ede9ec66e2d0462920dfd4c60bdcc412e082f96c855cb1dc9b3c1f9c1dbedd7`  
		Last Modified: Fri, 24 Jun 2022 03:07:43 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:887d01d0faac32364f7a82d3d4d4d224ab97e3ff6092b314772f1e768ddd8a6c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109968373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba4bb5600fd5c88b0588d2ae8e4c502374d5fe108bc2a73a9255e93405e24fb`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 May 2022 00:46:59 GMT
ADD file:158a0e401328bd7c0d49b9e8539186098967218f1b1a8c811f4398d29b74397f in / 
# Wed, 11 May 2022 00:47:00 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:48:02 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:48:03 GMT
ENV EMQX_VERSION=4.4.3
# Wed, 11 May 2022 01:48:04 GMT
ENV OTP=otp24.1.5-3
# Wed, 11 May 2022 01:48:09 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="7f7305566b977ef64afd31fed5fa71f7e79a5a934bf792422ac03e4f12768b02"; fi;     if [ ${arch} = "arm64" ]; then sha256="34d3315c329de1d0fbf7419db1bff5007313f45de39e8be0ca5f04bad19f45a5"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 May 2022 01:48:10 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 May 2022 01:48:11 GMT
WORKDIR /opt/emqx
# Wed, 11 May 2022 01:48:11 GMT
USER emqx
# Wed, 11 May 2022 01:48:12 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 May 2022 01:48:13 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 May 2022 01:48:15 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 May 2022 01:48:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 May 2022 01:48:16 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:dfdd5ffb257742b891ccad9400a77dad2a6260b2451e0f5e48a9ade1d17a87ec`  
		Last Modified: Wed, 11 May 2022 00:53:46 GMT  
		Size: 30.1 MB (30065693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41aff1a51b467f4353bb41440f62b9e619e628b9ae3dce9c015dba39d943604f`  
		Last Modified: Wed, 11 May 2022 01:48:35 GMT  
		Size: 2.4 MB (2351167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed44caa74811db97a6a7048b7d8ddb5a25e1edd000c0bdb89601c6de2974595`  
		Last Modified: Wed, 11 May 2022 01:48:39 GMT  
		Size: 38.8 MB (38773530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee8ec3642d256f9ca93285fc5fba425343ec272ce50c6c9dcb89ac4bf3a8925`  
		Last Modified: Wed, 11 May 2022 01:48:40 GMT  
		Size: 38.8 MB (38776875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e7077a80db19beb0214216aeaf4feac06e3b677d57a99c6853a0578717fe85`  
		Last Modified: Wed, 11 May 2022 01:48:34 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
