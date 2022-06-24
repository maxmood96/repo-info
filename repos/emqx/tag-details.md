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
$ docker pull emqx@sha256:0adb0c690c3b7cdaeef631a7a309253338877dc0c3172fb676f483657597aa29
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
$ docker pull emqx@sha256:08d3ac9d9898424f7bc01ee8227295723cbeb94ad7826cf1bbdf47209c9353bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110032671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5f41662c312d1f255f4b776418c63543d882d5efe5d4e2f03c5121bfac4336`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:43 GMT
ADD file:134be48af13f80f3474bf1b080ca781feb7b972148d482849862e55eb2acd61c in / 
# Thu, 23 Jun 2022 00:40:44 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:46:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 04:34:23 GMT
ENV EMQX_VERSION=4.4.4
# Fri, 24 Jun 2022 04:34:24 GMT
ENV OTP=otp24.1.5-3
# Fri, 24 Jun 2022 04:34:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Fri, 24 Jun 2022 04:34:30 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Fri, 24 Jun 2022 04:34:30 GMT
WORKDIR /opt/emqx
# Fri, 24 Jun 2022 04:34:31 GMT
USER emqx
# Fri, 24 Jun 2022 04:34:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 24 Jun 2022 04:34:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Fri, 24 Jun 2022 04:34:35 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Fri, 24 Jun 2022 04:34:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 24 Jun 2022 04:34:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:3b157c852f2736e12f09046f214fe5f6a0b1652bd860269b3988c92a197026e8`  
		Last Modified: Thu, 23 Jun 2022 00:47:22 GMT  
		Size: 30.1 MB (30065720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255b4cf5a20375604dbc0f926e6f813eaac7b8eb73cb515b6cd600e0b893e079`  
		Last Modified: Fri, 24 Jun 2022 04:35:11 GMT  
		Size: 2.4 MB (2351321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c225e8442bf2f752a21e3ad94f889218aff1262ead1862c6dc45363b62f61c0`  
		Last Modified: Fri, 24 Jun 2022 04:35:15 GMT  
		Size: 38.8 MB (38806768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c213270161d65a52f008d85d862aedc44a45ce3b813376c113118c8382db8`  
		Last Modified: Fri, 24 Jun 2022 04:35:15 GMT  
		Size: 38.8 MB (38807753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bf6ab71269c0efbbdf8ea7e821c2c938e996c9d2ff01536660ffa898cdd068`  
		Last Modified: Fri, 24 Jun 2022 04:35:11 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3`

```console
$ docker pull emqx@sha256:08c44a43f08be8eb6a2ddeb7f19750a5ccb051a1678c706c962f93c19bb48115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

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

### `emqx:4.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:160bdf8dd5dc020ea1f1c6eb95dbf0877ab8d0d338143234aa04db8237e3d12c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101935482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f920917e1fa4ead6941f60ed3f0dd73a3882279ea2e17c657a8eaee93ff341`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Fri, 24 Jun 2022 04:34:04 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 04:34:05 GMT
ENV EMQX_VERSION=4.3.15
# Fri, 24 Jun 2022 04:34:09 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Fri, 24 Jun 2022 04:34:10 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Fri, 24 Jun 2022 04:34:11 GMT
WORKDIR /opt/emqx
# Fri, 24 Jun 2022 04:34:11 GMT
USER emqx
# Fri, 24 Jun 2022 04:34:12 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 24 Jun 2022 04:34:13 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Fri, 24 Jun 2022 04:34:15 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Fri, 24 Jun 2022 04:34:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 24 Jun 2022 04:34:16 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13bdfece1acee3048217eedfbf5066ec26eea3c0c6eefac64ebcac2b13fb6d9`  
		Last Modified: Fri, 24 Jun 2022 04:34:56 GMT  
		Size: 4.5 MB (4485475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0cf700130db6c38f07fc3572565ec51944f477d64c9010d3600d4bf182a602`  
		Last Modified: Fri, 24 Jun 2022 04:35:00 GMT  
		Size: 35.8 MB (35761680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f9e4afd2fdc9093ff68cfcc24ccb8f8c4435099da66a47fc7eddbfc2b3e629`  
		Last Modified: Fri, 24 Jun 2022 04:35:00 GMT  
		Size: 35.8 MB (35773256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfdef4bf9324ad1eef1c0ce9dacb745b2227a70146e7dcb9988bffcecad8981`  
		Last Modified: Fri, 24 Jun 2022 04:34:56 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3.15`

```console
$ docker pull emqx@sha256:08c44a43f08be8eb6a2ddeb7f19750a5ccb051a1678c706c962f93c19bb48115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

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

### `emqx:4.3.15` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:160bdf8dd5dc020ea1f1c6eb95dbf0877ab8d0d338143234aa04db8237e3d12c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101935482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f920917e1fa4ead6941f60ed3f0dd73a3882279ea2e17c657a8eaee93ff341`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Fri, 24 Jun 2022 04:34:04 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 04:34:05 GMT
ENV EMQX_VERSION=4.3.15
# Fri, 24 Jun 2022 04:34:09 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Fri, 24 Jun 2022 04:34:10 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Fri, 24 Jun 2022 04:34:11 GMT
WORKDIR /opt/emqx
# Fri, 24 Jun 2022 04:34:11 GMT
USER emqx
# Fri, 24 Jun 2022 04:34:12 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 24 Jun 2022 04:34:13 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Fri, 24 Jun 2022 04:34:15 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Fri, 24 Jun 2022 04:34:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 24 Jun 2022 04:34:16 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13bdfece1acee3048217eedfbf5066ec26eea3c0c6eefac64ebcac2b13fb6d9`  
		Last Modified: Fri, 24 Jun 2022 04:34:56 GMT  
		Size: 4.5 MB (4485475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0cf700130db6c38f07fc3572565ec51944f477d64c9010d3600d4bf182a602`  
		Last Modified: Fri, 24 Jun 2022 04:35:00 GMT  
		Size: 35.8 MB (35761680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f9e4afd2fdc9093ff68cfcc24ccb8f8c4435099da66a47fc7eddbfc2b3e629`  
		Last Modified: Fri, 24 Jun 2022 04:35:00 GMT  
		Size: 35.8 MB (35773256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfdef4bf9324ad1eef1c0ce9dacb745b2227a70146e7dcb9988bffcecad8981`  
		Last Modified: Fri, 24 Jun 2022 04:34:56 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:0adb0c690c3b7cdaeef631a7a309253338877dc0c3172fb676f483657597aa29
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
$ docker pull emqx@sha256:08d3ac9d9898424f7bc01ee8227295723cbeb94ad7826cf1bbdf47209c9353bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110032671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5f41662c312d1f255f4b776418c63543d882d5efe5d4e2f03c5121bfac4336`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:43 GMT
ADD file:134be48af13f80f3474bf1b080ca781feb7b972148d482849862e55eb2acd61c in / 
# Thu, 23 Jun 2022 00:40:44 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:46:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 04:34:23 GMT
ENV EMQX_VERSION=4.4.4
# Fri, 24 Jun 2022 04:34:24 GMT
ENV OTP=otp24.1.5-3
# Fri, 24 Jun 2022 04:34:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Fri, 24 Jun 2022 04:34:30 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Fri, 24 Jun 2022 04:34:30 GMT
WORKDIR /opt/emqx
# Fri, 24 Jun 2022 04:34:31 GMT
USER emqx
# Fri, 24 Jun 2022 04:34:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 24 Jun 2022 04:34:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Fri, 24 Jun 2022 04:34:35 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Fri, 24 Jun 2022 04:34:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 24 Jun 2022 04:34:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:3b157c852f2736e12f09046f214fe5f6a0b1652bd860269b3988c92a197026e8`  
		Last Modified: Thu, 23 Jun 2022 00:47:22 GMT  
		Size: 30.1 MB (30065720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255b4cf5a20375604dbc0f926e6f813eaac7b8eb73cb515b6cd600e0b893e079`  
		Last Modified: Fri, 24 Jun 2022 04:35:11 GMT  
		Size: 2.4 MB (2351321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c225e8442bf2f752a21e3ad94f889218aff1262ead1862c6dc45363b62f61c0`  
		Last Modified: Fri, 24 Jun 2022 04:35:15 GMT  
		Size: 38.8 MB (38806768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c213270161d65a52f008d85d862aedc44a45ce3b813376c113118c8382db8`  
		Last Modified: Fri, 24 Jun 2022 04:35:15 GMT  
		Size: 38.8 MB (38807753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bf6ab71269c0efbbdf8ea7e821c2c938e996c9d2ff01536660ffa898cdd068`  
		Last Modified: Fri, 24 Jun 2022 04:35:11 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.4`

```console
$ docker pull emqx@sha256:0adb0c690c3b7cdaeef631a7a309253338877dc0c3172fb676f483657597aa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

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

### `emqx:4.4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:08d3ac9d9898424f7bc01ee8227295723cbeb94ad7826cf1bbdf47209c9353bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110032671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5f41662c312d1f255f4b776418c63543d882d5efe5d4e2f03c5121bfac4336`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:43 GMT
ADD file:134be48af13f80f3474bf1b080ca781feb7b972148d482849862e55eb2acd61c in / 
# Thu, 23 Jun 2022 00:40:44 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:46:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 04:34:23 GMT
ENV EMQX_VERSION=4.4.4
# Fri, 24 Jun 2022 04:34:24 GMT
ENV OTP=otp24.1.5-3
# Fri, 24 Jun 2022 04:34:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Fri, 24 Jun 2022 04:34:30 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Fri, 24 Jun 2022 04:34:30 GMT
WORKDIR /opt/emqx
# Fri, 24 Jun 2022 04:34:31 GMT
USER emqx
# Fri, 24 Jun 2022 04:34:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 24 Jun 2022 04:34:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Fri, 24 Jun 2022 04:34:35 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Fri, 24 Jun 2022 04:34:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 24 Jun 2022 04:34:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:3b157c852f2736e12f09046f214fe5f6a0b1652bd860269b3988c92a197026e8`  
		Last Modified: Thu, 23 Jun 2022 00:47:22 GMT  
		Size: 30.1 MB (30065720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255b4cf5a20375604dbc0f926e6f813eaac7b8eb73cb515b6cd600e0b893e079`  
		Last Modified: Fri, 24 Jun 2022 04:35:11 GMT  
		Size: 2.4 MB (2351321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c225e8442bf2f752a21e3ad94f889218aff1262ead1862c6dc45363b62f61c0`  
		Last Modified: Fri, 24 Jun 2022 04:35:15 GMT  
		Size: 38.8 MB (38806768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c213270161d65a52f008d85d862aedc44a45ce3b813376c113118c8382db8`  
		Last Modified: Fri, 24 Jun 2022 04:35:15 GMT  
		Size: 38.8 MB (38807753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bf6ab71269c0efbbdf8ea7e821c2c938e996c9d2ff01536660ffa898cdd068`  
		Last Modified: Fri, 24 Jun 2022 04:35:11 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:0adb0c690c3b7cdaeef631a7a309253338877dc0c3172fb676f483657597aa29
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
$ docker pull emqx@sha256:08d3ac9d9898424f7bc01ee8227295723cbeb94ad7826cf1bbdf47209c9353bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110032671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5f41662c312d1f255f4b776418c63543d882d5efe5d4e2f03c5121bfac4336`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:43 GMT
ADD file:134be48af13f80f3474bf1b080ca781feb7b972148d482849862e55eb2acd61c in / 
# Thu, 23 Jun 2022 00:40:44 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:46:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 04:34:23 GMT
ENV EMQX_VERSION=4.4.4
# Fri, 24 Jun 2022 04:34:24 GMT
ENV OTP=otp24.1.5-3
# Fri, 24 Jun 2022 04:34:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Fri, 24 Jun 2022 04:34:30 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Fri, 24 Jun 2022 04:34:30 GMT
WORKDIR /opt/emqx
# Fri, 24 Jun 2022 04:34:31 GMT
USER emqx
# Fri, 24 Jun 2022 04:34:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 24 Jun 2022 04:34:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Fri, 24 Jun 2022 04:34:35 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Fri, 24 Jun 2022 04:34:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 24 Jun 2022 04:34:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:3b157c852f2736e12f09046f214fe5f6a0b1652bd860269b3988c92a197026e8`  
		Last Modified: Thu, 23 Jun 2022 00:47:22 GMT  
		Size: 30.1 MB (30065720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255b4cf5a20375604dbc0f926e6f813eaac7b8eb73cb515b6cd600e0b893e079`  
		Last Modified: Fri, 24 Jun 2022 04:35:11 GMT  
		Size: 2.4 MB (2351321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c225e8442bf2f752a21e3ad94f889218aff1262ead1862c6dc45363b62f61c0`  
		Last Modified: Fri, 24 Jun 2022 04:35:15 GMT  
		Size: 38.8 MB (38806768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c213270161d65a52f008d85d862aedc44a45ce3b813376c113118c8382db8`  
		Last Modified: Fri, 24 Jun 2022 04:35:15 GMT  
		Size: 38.8 MB (38807753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bf6ab71269c0efbbdf8ea7e821c2c938e996c9d2ff01536660ffa898cdd068`  
		Last Modified: Fri, 24 Jun 2022 04:35:11 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
